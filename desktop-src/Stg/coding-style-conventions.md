---
title: Codierungsstil Konventionen
description: Codierungsstil Konventionen werden in dieser Beispiel Reihe verwendet, um Klarheit und Konsistenz zu gewährleisten.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734961"
---
# <a name="coding-style-conventions"></a>Codierungsstil Konventionen

Codierungsstil Konventionen werden in dieser Beispiel Reihe verwendet, um Klarheit und Konsistenz zu gewährleisten. Die Konventionen für die "ungarisch"-Notation werden verwendet. Diese wurden in der Win32-Programmierung häufig zum Codierungs Verhalten. Sie enthalten Variablen Präfix-Notationen, die Variablennamen einen Vorschlag des Typs der Variablen geben.

In der folgenden Tabelle sind allgemeine Präfixe aufgeführt.



| Präfix | BESCHREIBUNG                         |
|--------|-------------------------------------|
| a      | Array                               |
| b      | Bool (int)                          |
| c      | Char                                |
| betrieben     | Anzahl von Bytes                      |
| cr     | Farb Verweis Wert               |
| verschoben     | Anzahl von x (Short)                  |
| dw     | DWORD (unsigned long)               |
| f      | Flags (in der Regel mehrere Bitwerte) |
| fn     | Funktion                            |
| selbst\_    | Global                              |
| h.      | Handle                              |
| i      | Integer                             |
| l      | Long                                |
| lp     | Long-Zeiger                        |
| 800\_    | Datenmember einer Klasse              |
| n      | Short int                           |
| p      | Zeiger                             |
| s      | String                              |
| sz     | NULL beendete Zeichenfolge              |
| tm     | Textmetrik                         |
| u      | Unsigned int                        |
| nützlichen     | Unsigned long (ULONG)               |
| w      | Word (kurz ohne Vorzeichen)               |
| x, y    | x, y-Koordinaten (kurz)            |



 

Diese werden häufig kombiniert, wie im folgenden.



| Präfix Kombination | BESCHREIBUNG                                             |
|--------------------|---------------------------------------------------------|
| pszmystring        | Ein Zeiger auf eine Zeichenfolge.                                  |
| m \_ pszmystring     | Ein Zeiger auf eine Zeichenfolge, die ein Datenmember einer Klasse ist. |



 

In der folgenden Tabelle sind andere Konventionen aufgeführt.



| Konvention       | BESCHREIBUNG                                              |
|------------------|----------------------------------------------------------|
| CMyClass         | Präfix "C" für C++-Klassennamen.                          |
| Comyobjectclass  | Präfix ' Co ' für COM-Objektklassen Namen.                  |
| Cfmyclassfactory | Präfix ' CF ' für com-klassenfactorynamen.                 |
| Imeineschnittstelle     | Präfix "I" für Namen der COM-Schnittstellen Klasse.                |
| Cimpimyinterface | Präfix ' cimpi ' für Implementierungsklassen der COM-Schnittstelle. |



 

Einige konsistente Konventionen für Kommentar Header Blöcke werden wie folgt in dieser Beispiel Reihe verwendet.

## <a name="file-header"></a>Datei Header

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a>Block "Plain comment"

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>Klassen Deklarations Header

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a>Klassen Methoden-Definitions Header

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a>Nicht exportierte oder lokale Funktion

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a>Definitions Header der exportierten Funktion

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a>Deklaration der COM-Schnittstelle

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a>COM-Objektklassen Deklarations Header

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

Alle diese Kommentar Block Konventionen haben konsistente Anfangs-und Endtoken-Zeichen folgen. Diese Konsistenz unterstützt die automatische Verarbeitung der Header auf irgendeine Weise. Beispielsweise können awk-Skripts geschrieben werden, um die Funktions Header in eine separate Textdatei zu filtern, die als Grundlage für ein Spezifikationsdokument dienen kann. Ebenso können Tools wie das nicht unterstützte autoduck-Hilfsprogramm (zurzeit auf der Microsoft Developer Network Development Library-CD-ROM verfügbar) zum Verarbeiten der Kommentar Blöcke in diesen Headern verwendet werden.

In der folgenden Tabelle werden die in Beispiel Lernprogrammen verwendeten Zeichen folgen für den Anfang und das Beenden aufgeführt



| Token | BESCHREIBUNG                      |
|-------|----------------------------------|
| /\*+  | Datei Header Anfang                |
| +\*/  | Datei Header Ende                  |
| /\*-  | Anfang der Block Kopfzeile für Klartext |
| -\*/  | Ende der Block Kopfzeile des Plain comment   |
| /\*Scher  | Klassen Header Anfang               |
| Scher\*/  | Header Ende der Klasse                 |
| /\*800  | Methoden Header Anfang              |
| 800\*/  | Methoden Header Ende                |
| /\*C  | Funktions Header Anfang            |
| C\*/  | Funktions Header Ende              |
| /\*Ich  | Schnittstellen-Header Anfang           |
| Ich\*/  | Schnittstellen-Header Ende             |
| /\*'  | Anfang der com-Objektklassen Kopfzeile    |
| '\*/  | Header Ende der com-Objektklasse      |



 

Diese Header können auch als visuelle Hinweise für das schnelle Scannen von Quelldateien verwendet werden. Außerdem bieten Sie Ihnen die Möglichkeit, schnell zu einem Quell Speicherort zu gelangen, wenn Sie Such Zeichenfolgen in Ihrem Editor einrichten und dann "Letzte Suche" wiederholen, um diese Header schnell zu finden.

Die Such Zeichenfolge "m + M" findet z. b. den Anfang von Methoden Headern, und "m-m" findet den Anfang des tatsächlichen Methoden Definitions-/Implementierungs Codes.

 

 




