---
description: Vorlagen definieren, wie der Datenstrom interpretiert wird. die Daten werden von der Vorlagen Definition moduliert. In diesem Abschnitt werden die folgenden Aspekte einer Vorlage erläutert und eine Beispiel Vorlage bereitstellt.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Vorlagen (X-Dateiformat, Text Codierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745392"
---
# <a name="templates-x-file-format-text-encoding"></a>Vorlagen (X-Dateiformat, Text Codierung)

Vorlagen definieren, wie der Datenstrom interpretiert wird. die Daten werden von der Vorlagen Definition moduliert. In diesem Abschnitt werden die folgenden Aspekte einer Vorlage erläutert und eine Beispiel Vorlage bereitstellt.

Es gibt eine besondere Vorlage (die Header Vorlage). Es wird empfohlen, dass jede Anwendung eine Header Vorlage definiert und Sie zum Definieren von anwendungsspezifischen Informationen verwendet, z. b. Versionsinformationen. Wenn dieser Header vorhanden ist, wird er von der. x-Dateiformat-API gelesen. Wenn ein Flags-Member verfügbar ist, wird er verwendet, um zu bestimmen, wie die folgenden Daten interpretiert werden. Der Flags-Member sollte, falls definiert, ein DWORD-Element sein. Zurzeit ist ein Bit definiert-Bit 0. Wenn dieses Bit eindeutig ist, sind die folgenden Daten in der Datei binär. Wenn festgelegt, sind die folgenden Daten Text. Sie können mehrere Header Datenobjekte verwenden, um zwischen Binärdateien und Text in der Datei zu wechseln.

## <a name="template-form-name-and-uuid"></a>Vorlagen Formular, Name und UUID

Eine Vorlage weist das folgende Format auf.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



Der Vorlagen Name ist ein alphanumerischer Name, der den Unterstrich () enthalten kann \_ . Er darf nicht mit einer Ziffer beginnen. Die UUID ist ein universell eindeutiger Bezeichner, der für den Standard der verteilten Computing-Umgebung von Open Software Foundation formatiert und durch eckige Klammern (< >) eingeschlossen wird. Beispiel: <3d82ab43-62da-11CF-ab39-0020af71e433>.

## <a name="template-members"></a>Vorlagen Mitglieder

Vorlagen Elemente bestehen aus einem benannten Datentyp, gefolgt von einem optionalen Namen oder einem Array eines benannten Datentyps. Gültige primitive Datentypen sind in der folgenden Tabelle definiert.



| type    | Size                               |
|---------|------------------------------------|
| WORD    | 16 Bit                            |
| DWORD   | 32 Bit                            |
| GLEITKOMMAZAHL   | IEEE Float                         |
| Double  | 64 Bit                            |
| CHAR    | 8 Bit                             |
| UCHAR   | 8 Bit                             |
| BYTE    | 8 Bit                             |
| STRING  | NULL beendete Zeichenfolge             |
| CSTRING | Formatierte C-Zeichenfolge (nicht unterstützt) |
| UNICODE | Unicode-Zeichenfolge (nicht unterstützt)     |



 

Auf zusätzliche Datentypen, die durch Vorlagen definiert werden, die zuvor im Datenstrom definiert wurden, kann auch innerhalb einer Vorlagen Definition referenziert werden. Es sind keine vorwärts Verweise zulässig.

Jeder gültige Datentyp kann als Array in der Vorlagen Definition ausgedrückt werden. Die grundlegende Syntax wird im folgenden Beispiel gezeigt.


```
array <data-type> <name>[<dimension-size>];
```



<Dimensions Größe> kann entweder eine ganze Zahl oder ein benannter Verweis auf einen anderen Vorlagen Member sein, dessen Wert dann ersetzt wird. Arrays können n-dimensional sein, wobei n durch die Anzahl der gekoppelten eckigen Klammern bestimmt wird, die der Anweisung folgen, wie im folgenden Beispiel gezeigt.


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>Vorlagen Einschränkungen

Vorlagen können offen, geschlossen oder eingeschränkt sein. Diese Einschränkungen legen fest, welche Datentypen in der unmittelbaren Hierarchie eines von der Vorlage definierten Datenobjekts vorkommen können. Eine geöffnete Vorlage hat keine Einschränkungen, eine geschlossene Vorlage lehnt alle Datentypen ab, und eine eingeschränkte Vorlage lässt eine benannte Liste von Datentypen zu.

Die Syntax zum Angeben einer geöffneten Vorlage besteht aus drei Punkten, die in eckigen Klammern eingeschlossen sind.


```
[ ... ]
```



Eine durch Trennzeichen getrennte Liste benannter Datentypen, gefolgt von ihren UUIDs, die in eckigen Klammern eingeschlossen sind, deutet auf eine eingeschränkte Vorlage hin.


```
[ { data-type [ UUID ] , } ... ]
```



Das Fehlen einer der obigen Optionen deutet auf eine geschlossene Vorlage hin.

## <a name="template-example"></a>Vorlagen Beispiel

Das folgende Beispiel zeigt eine Beispiel Vorlage.


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text Codierung](text-encoding.md)
</dt> </dl>

 

 



