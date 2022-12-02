<template>
  <v-app id="inspire">
    <v-dialog
      v-model="privacidad"
      width="700"
      persistent
    >
      <v-card>
        <v-card-title class="text-h5 grey lighten-2">
          Privacy Policy
        </v-card-title>

        <v-card-text>
          La Universidad de Sonora, con domicilio en Boulevard Luis Encinas Johnson y Rosales, S/N, Colonia Centro, en Hermosillo, Sonora; de conformidad con los artículos sexto, apartado A, fracción II y 16 párrafo segundo de la Constitución Política de los Estados Unidos Mexicanos, así como los artículos tercero fracción XXVIII y demás establecidos dentro del título segundo de la Ley General de Protección de Datos Personales en Posesión de Sujetos Obligados, es la responsable del tratamiento de sus datos personales, los cuales serán protegidos conforme a las disposiciones establecidas dentro de la Ley General de Protección de Datos Personales en Posesión de Sujetos Obligados, así como la normatividad aplicable.

De acuerdo a los artículos  tercero fracción XXVIII;  artículo 2, apartado A, de la Constitución Política del Estado de Sonora; así como el artículo 3, fracciones IX y X, de la Ley General de Protección de Datos Personales en Posesión de Sujetos Obligados; artículo 3 fracciones VII y VIII de la Ley  número 192 de Protección de Datos Personales en Posesión de Sujetos Obligados del Estado de Sonora; y de acuerdo a la normatividad interna, en su artículo segundo, fracción IV, de los Lineamientos para la Transparencia y Acceso a la Información en la Universidad de Sonora; se hace de su conocimiento que se considerará información confidencial cualquier información concerniente a una persona física identificada o identificable expresada en forma numérica, alfabética, alfanumérica, gráfica, fotográfica, acústica o en cualquier otro formato. Se considera que una persona es identificable cuando su identidad puede determinarse directa o indirectamente a través de cualquier información, siempre y cuando esto no requiera plazo, medios o actividades desproporcionadas.  De igual forma, deberá entenderse por datos sensibles aquellos que se refieran a la esfera más íntima de su titular, o cuya utilización indebida pueda dar origen a discriminación o conlleve un riesgo grave para éste.  De manera enunciativa más no limitativa, se consideran sensibles los datos personales que puedan revelar aspectos como origen racial o étnico, estado de salud presente o futuro, información genética, creencias religiosas, filosóficas y morales, opiniones políticas y preferencia sexual.

La Universidad de Sonora, podrá dar tratamiento a sus datos personales de acuerdo a finalidades distintas aquellas establecidas en el presente aviso de privacidad, de acuerdo a las atribuciones conferidas en la Ley Número 4 Orgánica de la Universidad de Sonora, y su Estatuto General, así como la demás normatividad interna de la Institución. Entendiendo al tratamiento como cualquier operación o conjunto de operaciones efectuadas mediante procedimientos físicos o automatizados aplicados a los datos personales, relacionadas, de manera enunciativa más no limitativa, con la obtención, uso, registro, organización, conservación, elaboración, utilización, estructuración, adaptación, modificación, extracción, consulta, comunicación, difusión, almacenamiento, posesión, acceso, manejo, aprovechamiento, transferencia y en general cualquier uso o disposición.

Los datos personales que se recaben por la Institución podrán ser sometidos a tratamiento, y serán única y exclusivamente utilizados para los fines que fueron proporcionados, de acuerdo con sus objetivos y facultades establecidas detalladamente en los artículos 5, 6 y 7 de la Ley Número 4 Orgánica de la Universidad de Sonora, artículos 1 y 2 del Estatuto General y los artículos 26 y 84 del Reglamento Escolar de la Universidad de Sonora, así como para la prestación de los servicios que Institución ofrece conforme a las unidades de apoyo establecidas en el artículo 4 y 5 del Estatuto General; datos que estarán a resguardo y protección de las mismas.

Los datos personales requeridos para el cumplimiento de las funciones ofrecidas por la Institución, serán los siguientes: nombre, edad, domicilio particular, nacionalidad, estado civil, teléfono particular y dirección de correo electrónico.

De manera excepcional se requerirán datos personales sensibles tales como: estado de salud físico o si pertenece a algún grupo étnico; mismos que serán altamente protegidos.

Se informa que la Universidad de Sonora no hará transferencia de datos personales, salvo aquellas que sean necesarias para atender requerimientos de información de una autoridad competente, siempre y cuando estén fundados y motivados, o se actualice alguno de los supuestos establecidos dentro de los artículos 70 de la Ley General de Protección de Datos Personales en Posesión de Sujetos Obligados, así como el artículo 97 de la Ley de Protección de datos personales en posesión de Sujetos Obligados del Estado de Sonora.

Por otra parte, se le hace saber que de acuerdo al artículo 22 de la Ley General de Protección de Datos Personales en Posesión de Sujetos Obligados, sus datos personales pueden ser tratados sin autorización del titular, en los siguientes casos:

Cuando una ley así lo disponga, debiendo dichos supuestos ser acordes con las bases, principios y disposiciones establecidos en esta Ley. En ningún caso, podrán contravenirla;
Cuando las transferencias que se realicen entre responsables sean sobre datos personales que se utilicen para el ejercicio de facultades propias, compatibles o análogas con la finalidad que motivó el tratamiento de los datos personales;
Cuando exista una orden judicial, resolución o mandato fundado y motivado de autoridad competente;
Para el reconocimiento o defensa de derechos del titular ante autoridad competente;
Cuando los datos personales se requieran para ejercer un derecho o cumplir obligaciones derivadas de una relación jurídica entre el titular y el responsable;
Cuando exista una situación de emergencia que potencialmente pueda dañar a un individuo en su persona en sus bienes;
Cuando los datos personales sean necesarios para efectuar un tratamiento para la prevención, diagnóstico, la prestación de asistencia sanitaria;
Cuando los datos personales figuren en fuentes de acceso público;
Cuando los datos personales se sometan a un procedimiento previo de disociación, o;
Cuando el titular de los datos personales sea una persona reportada como desaparecida en los términos de la ley en la materia.

        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="privacidad = false"
          >
            I accept
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
    <v-navigation-drawer
      v-model="drawer"
      :clipped="$vuetify.breakpoint.lgAndUp"
      app
      color="grey darken-3"
    >
      <v-list dense color="grey darken-3">
        <v-divider class="mt-3"></v-divider>
        <template>
          <v-list-group
            v-for="item in items"
            :key="item.text"
            v-model="item.model"
            :prepend-icon="['mdi-clipboard-text']"
            append-icon=""
            active-class="primary darken-4"
          >
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title class="white--text">
                  {{ item.text }}
                </v-list-item-title>
              </v-list-item-content>
            </template>
          </v-list-group>
        </template>
        <v-divider></v-divider>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      :clipped-left="$vuetify.breakpoint.lgAndUp"
      app
      color="primary"
      dark
      dense
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title style="width: 600px">
        <router-link
          to="/engorda/home"
          exact
          class="white--text text-decoration-none mr-2"
        >
          <v-icon class="mb-1 mr-2">mdi-home</v-icon>
        </router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <div class="text-center">
        <span>Usuario</span>
        <v-bottom-sheet v-model="sheet">
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="grey darken-3"
              v-bind="attrs"
              v-on="on"
              small
              fab
              elevation="2"
              class="ml-2"
            >
              <v-icon>mdi-account-circle</v-icon>
            </v-btn>
          </template>
          <v-list>
            <v-subheader>Menu de usuario</v-subheader>
            <v-list-item
              v-for="tile in tiles"
              :key="tile.title"
              @click="sheet = false"
            >
              <v-list-item-avatar>
                <v-avatar size="32px" tile>
                  <router-link
                    :to="tile.href"
                    class="grey--text text-decoration-none"
                  >
                    <v-icon>{{ tile.icon }}</v-icon>
                  </router-link>
                </v-avatar>
              </v-list-item-avatar>
              <v-list-item-title>
                <router-link
                  :to="tile.href"
                  class="grey--text text-decoration-none"
                  active-class="primary--text"
                >
                  {{ tile.title }}
                </router-link>
              </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-bottom-sheet>
      </div>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <v-expand-transition>
          <router-view></router-view>
        </v-expand-transition>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    privacidad: true,
    dialog: false,
    drawer: false,
    sheet: false,
    tiles: [
      { icon: "mdi-account-cog", title: "Panel Administrador", href: "/panelAdmin/panelControl" },
      { icon: "mdi-exit-to-app", title: "Salir del sistema", href: "/" },
    ],
    items: [
      {
        text: "De todos los temas",
        model: true,
      },
    ],
  }),
};
</script>
<style scoped>
.container {
  max-width: 1600px;
}
</style>