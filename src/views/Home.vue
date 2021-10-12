<template>
  <div class="container">
    <div class="row">
      <div class="col-sm-10">
        <h1>Заметки</h1>
        <hr />
        <br /><br />
        <button type="button" class="btn btn-success btn-sm">
          Добавить заметку
        </button>
        <br /><br />
        <table class="table table-hover">
          <thead>
            <tr>
              <th scope="col">Заголовок</th>
              <th scope="col">Заметка</th>
              <th scope="col">Дата создания</th>
              <th></th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(note, index) in notes" :key="index">
              <td>{{ note.title }}</td>
              <td>{{ note.body }}</td>
              <td>{{ note.createTime }}</td>
              <td>
                <button type="button" class="btn btn-warning btn-sm">
                  Изменить
                </button>
                <button type="button" class="btn btn-danger btn-sm">
                  Удалить
                </button>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
<<<<<<< Updated upstream

=======
>>>>>>> Stashed changes
    <!-- <b-modal
      ref="addBookModal"
      id="book-modal"
      title="Add a new book"
      hide-footer
    >
      <b-form @submit="onSubmit" @reset="onReset" class="w-100">
        <b-form-group
          id="form-title-group"
          label="Title:"
          label-for="form-title-input"
        >
          <b-form-input
            id="form-title-input"
            type="text"
            v-model="addBookForm.title"
            required
            placeholder="Enter title"
          >
          </b-form-input>
        </b-form-group>
        <b-form-group
          id="form-author-group"
          label="Author:"
          label-for="form-author-input"
        >
          <b-form-input
            id="form-author-input"
            type="text"
<<<<<<< Updated upstream
            v-model="addBookForm.author"
=======
            v-model="addNoteMForm.author"
>>>>>>> Stashed changes
            required
            placeholder="Enter author"
          >
          </b-form-input>
        </b-form-group>
        <b-form-group id="form-read-group">
          <b-form-checkbox-group v-model="addBookForm.read" id="form-checks">
            <b-form-checkbox value="true">Read?</b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>
        <b-button type="submit" variant="primary">Submit</b-button>
        <b-button type="reset" variant="danger">Reset</b-button>
      </b-form>
    </b-modal> -->
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      notes: [],
<<<<<<< Updated upstream
      addNoteForm: {
        Title: '',
        Body: '',
        CreateTime: '',
=======
      addNoteMForm: {
        title: '',
        author: '',
        read: [],
>>>>>>> Stashed changes
      },
    };
  },
  methods: {
<<<<<<< Updated upstream
    getNotes() {
      const path = "http://localhost:52362/api/Notes";
      axios
        .get(path)
=======
    getNoteMs() {
      const path = 'http://localhost:64960/api/NoteMs';
      axios.get(path)
>>>>>>> Stashed changes
        .then((res) => {
          this.notes = res.data;
        })
        .catch((err) => {
          // eslint-отключение следующей строки
          console.error(err);
        });
    },
<<<<<<< Updated upstream
    // addNote(payload) {
    //   const path = 'http://localhost:50898/api/Notes';
    //   axios.post(path, payload)
    //     .then(() => {
    //       this.getNotes();
    //     })
    //     .catch((error) => {
    //       // eslint-отключение следующей строки
    //       console.log(error);
    //       this.getNotes();
    //     });
    // },
    // initForm() {
    //   this.addNoteForm.Title = '';
    //   this.addNoteForm.Body = '';
    //   this.addNoteForm.CreateTime = '';
    // },
    // onSubmit(evt) {
    //   evt.preventDefault();
    //   this.$refs.addBookModal.hide();

    //   const payload = {
    //     Title: this.addNoteForm.Title,
    //     Body: this.addNoteForm.Body,
    //     CreateTime: this.addNoteForm.CreateTime,
    //   };

    //   this.addNote(payload);
    //   this.initForm();
    // },
    // onReset(evt) {
    //   evt.preventDefault();
    //   this.$refs.addBookModal.hide();
    //   this.initForm();
    // },
  },
=======
  //   addNoteM(payload) {
  //     const path = 'http://localhost:64960/api/NoteMs';
  //     axios.post(path, payload)
  //       .then(() => {
  //         this.getNoteMs();
  //       })
  //       .catch((error) => {
  //         // eslint-отключение следующей строки
  //         console.log(error);
  //         this.getNoteMs();
  //       });
  //   },
  //   initForm() {
  //     this.addNoteMForm.Title = '';
  //     this.addNoteMForm.Body = '';
  //     this.addNoteMForm.CreateDate = '';
  //   },
  //   onSubmit(evt) {
  //     evt.preventDefault();
  //     this.$refs.addBookModal.hide();
  //     const payload = {
  //       Title: this.addNoteMForm.Title,
  //       Body: this.addNoteMForm.Body,
  //       CreateTime:this.addNoteMForm.CreateDate, // сокращённое свойство
  //     };
  //     this.addNoteM(payload);
  //     this.initForm();
  //   },
  //   onReset(evt) {
  //     evt.preventDefault();
  //     this.$refs.addBookModal.hide();
  //     this.initForm();
  //   },
    },
>>>>>>> Stashed changes
  created() {
    this.getNoteMs();
  },
};
</script>

<style>
</style>