---
title: Konventionen für Codierungsstile
description: Codierungsstilkonventionen werden in dieser Beispielreihe verwendet, um Klarheit und Konsistenz zu unterstützen.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6f45fcff7e8f5f8e6f152ec1449bdf12170028537fd4b579d25479572dc5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962440"
---
# <a name="coding-style-conventions"></a>Konventionen für Codierungsstile

Codierungsstilkonventionen werden in dieser Beispielreihe verwendet, um Klarheit und Konsistenz zu unterstützen. Die Notationskonventionen für "Ungarisch" werden verwendet. Diese haben sich zu einer gängigen Programmierpraktiken bei der Win32-Programmierung entwickelt. Sie enthalten Variablenpräfix-Notationen, die Variablennamen einen Vorschlag vom Typ der Variablen geben.

In der folgenden Tabelle sind allgemeine Präfixe aufgeführt.



| Präfix | BESCHREIBUNG                         |
|--------|-------------------------------------|
| a      | Array                               |
| b      | BOOL (int)                          |
| c      | Char                                |
| Cb     | Anzahl der Bytes                      |
| cr     | Farbverweiswert               |
| Cx     | Anzahl von x (kurz)                  |
| dw     | DWORD (unsigned long)               |
| f      | Flags (in der Regel mehrere Bitwerte) |
| fn     | Funktion                            |
| G\_    | Global                              |
| h      | Handle                              |
| i      | Integer                             |
| l      | Long                                |
| lp     | Langer Zeiger                        |
| M\_    | Datenmember einer Klasse              |
| n      | Short int                           |
| p      | Zeiger                             |
| s      | String                              |
| sz     | 0 (null) beendete Zeichenfolge              |
| tm     | Textmetrik                         |
| u      | Unsigned int                        |
| Ul     | Unsigned long (ULONG)               |
| w      | WORD (unsigned short)               |
| x,y    | x- und y-Koordinaten (kurz)            |



 

Diese werden häufig wie im folgenden Beispiel kombiniert.



| Präfixkombination | Beschreibung                                             |
|--------------------|---------------------------------------------------------|
| pszMyString        | Ein Zeiger auf eine Zeichenfolge.                                  |
| m \_ pszMyString     | Ein Zeiger auf eine Zeichenfolge, die ein Datenmember einer Klasse ist. |



 

Andere Konventionen sind in der folgenden Tabelle aufgeführt.



| Konvention       | Beschreibung                                              |
|------------------|----------------------------------------------------------|
| CMyClass         | Präfix "C" für C++-Klassennamen.                          |
| COMyObjectClass  | Präfix "CO" für COM-Objektklassennamen.                  |
| CFMyClassFactory | Präfix 'CF' für COM-Klassenfactorynamen.                 |
| IMyInterface     | Präfix "I" für Com-Schnittstellenklassennamen.                |
| CImpIMyInterface | Präfix "CImpI" für IMPLEMENTIERUNGsklassen der COM-Schnittstelle. |



 

Einige konsistente Konventionen für Kommentarheaderblöcke werden in dieser Beispielreihe wie folgt verwendet.

## <a name="file-header"></a>Dateiheader

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

## <a name="plain-comment-block"></a>Plain Comment Block

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>Klassendeklarationsheader

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

## <a name="class-method-definition-header"></a>Klassenmethodendefinitionsheader

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

## <a name="exported-function-definition-header"></a>Exportierter Funktionsdefinitionsheader

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

## <a name="com-interface-declaration-header"></a>COM-Schnittstellendeklarationsheader

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

## <a name="com-object-class-declaration-header"></a>COM-Objektklassendeklarationsheader

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

Alle diese Kommentarblockkonventionen verfügen über konsistente Anfangs- und Endtokenzeichenfolgen. Diese Konsistenz unterstützt die automatische Verarbeitung der Header in irgendeiner Weise. Beispielsweise können AWK-Skripts geschrieben werden, um die Funktionsheader in eine separate Textdatei zu filtern, die dann als Grundlage für ein Spezifikationsdokument dienen kann. Ebenso können Tools wie das nicht unterstützte AUTODUCK-Hilfsprogramm (derzeit auf der CD-ROM der Microsoft-Entwickler Network Development Library verfügbar) verwendet werden, um die Kommentarblöcke in diesen Headern zu verarbeiten.

In der folgenden Tabelle sind die in Beispieltutorials verwendeten Anfangs- und Endtokenzeichenfolgen aufgeführt.



| Token | BESCHREIBUNG                      |
|-------|----------------------------------|
| /\*+  | File Header Begin                |
| +\*/  | Dateiheaderende                  |
| /\*-  | Plain comment block Header Begin |
| -\*/  | Einfaches Kommentarblock-Headerend   |
| /\*C  | Klassenheader Begin               |
| C\*/  | Klassenheaderende                 |
| /\*M  | Method Header Begin              |
| M\*/  | Methodenheaderende                |
| /\*F  | Start des Funktionsheaders            |
| F\*/  | Funktionsheaderende              |
| /\*Ich  | Interface Header Begin           |
| Ich\*/  | Schnittstellenheaderende             |
| /\*O  | COM Object Class Header Begin    |
| O\*/  | Headerende der COM-Objektklasse      |



 

Diese Header können auch als visuelle Hinweise für die schnelle Überprüfung von Quelldateien verwendet werden. Sie bieten auch die Vereinfachung, schnell zu einem Bestimmten Quellspeicherort zu kommen, wenn Sie Suchzeichenfolgen in Ihrem Editor einrichten und dann die letzte Suche wiederholen, um diese Header schnell zu finden.

Die Suchzeichenfolge "M+M" sucht beispielsweise den Anfang der Methodenheader, und "M-M" findet den Anfang der tatsächlichen Methodendefinition bzw. des Implementierungscodes.

 

 




