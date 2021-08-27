---
title: Verwenden von MIDL
description: Erstellen und Kompilieren einer MICROSOFT INTERFACE DEFINITION LANGUAGE-Schnittstelle (MIDL) und eines Remoteprozeduraufrufs (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ae89a740831fef28ade4c07dc6bbe2b9b68a8a154eb119f47e16b2cb68b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010748"
---
# <a name="using-midl"></a>Verwenden von MIDL

Alle Schnittstellen für Programme, die RPC verwenden, müssen in Microsoft Interface Definition Language (MIDL) definiert und mit dem MIDL-Compiler kompiliert werden. Die folgenden Themen stellen eine kurze Übersicht über das Erstellen und Kompilieren einer MIDL-Schnittstelle bereit:

-   [Definieren einer Schnittstelle mit MIDL](#defining-an-interface-with-midl)
-   [Kompilieren einer MIDL-Datei](#compiling-a-midl-file)

Eine ausführliche Erläuterung dieser Themen finden Sie unter [The IDL and ACF Files](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Definieren einer Schnittstelle mit MIDL

MIDL-Dateien sind Textdateien, die Sie mit einem Text-Editor erstellen und bearbeiten können. Wenn Sie eine UUID für Ihre Schnittstelle generieren, speichern Sie die Ausgabe in der Regel in einer MIDL-Vorlagendatei. Weitere Informationen zu UUIDs finden Sie unter [Generieren von Schnittstellen-UUIDs.](generating-interface-uuids.md)

Alle Schnittstellen in MIDL haben das gleiche Format. Sie beginnen mit einem Header, der eine Liste von Schnittstellenattributen und den Schnittstellennamen enthält. Die Attribute sind in eckige Klammern eingeschlossen. Auf den Schnittstellenheader folgt der Text, der in eckige Klammern eingeschlossen ist. Eine einfache Schnittstelle wird im folgenden Beispiel gezeigt:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

Einige der Attribute, die in der Regel in einer MIDL-Schnittstellendefinition enthalten sind, sind die UUID und die Versionsnummer der Schnittstelle. Der Text der Schnittstellendefinition muss die Prozedurdeklarationen aller Remoteprozeduren in der Schnittstelle enthalten. Sie kann auch die Deklarationen von Datentypen und Konstanten enthalten, die für die Schnittstelle erforderlich sind.

Alle Parameter in den Remoteprozedurdeklarationen müssen \[ [**als in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl)oder \] in \[ **,** out deklariert **werden.** \] Diese Deklarationen geben an, dass das Clientprogramm Daten an eine Remoteprozedur übergibt, Daten aus einer Remoteprozedur oder beides abfährt. Ausführlichere Informationen zu Schnittstellenparameterdeklarationen finden Sie unter [Der IDL-Schnittstellenkörper.](the-idl-interface-body.md)

## <a name="compiling-a-midl-file"></a>Kompilieren einer MIDL-Datei

Der MIDL-Compiler ist ein Befehlszeilentool, das automatisch mit dem Platform Software Development Kit (SDK) installiert wird. Rufen Sie ihn in einem Befehlsfenster auf, indem Sie den Befehl **midl** gefolgt vom Namen einer MIDL-Datei in der Befehlszeile eingeben. Stellen Sie sicher, dass sich das Verzeichnis mit dem MIDL-Compiler in Ihrem Pfad befindet. Im folgenden Beispiel wird die Verwendung veranschaulicht:

**midl MyApp.idl**

Beachten Sie, dass Sie die Erweiterung nicht angeben müssen, wenn der Dateiname die Erweiterung .idl hat. Sie können auch die [MIDL-Compilerbefehlszeilenschalter](/windows/desktop/Midl/midl-command-line-reference) verwenden, indem Sie sie zwischen dem **midl-Befehl** und dem Dateinamen einfügen. Dies wird im folgenden Beispiel gezeigt:

**midl /acf MyApp.acf MyApp.idl**

In diesem Beispiel wird der MIDL-Compiler mit der Datei MyApp.idl als Eingabedatei ausgeführt. Der Befehlszeilenschalter **/acf** weist den Compiler an, auch eine Anwendungskonfigurationsdatei (Application Configuration File, ACF) für die Eingabe zu verwenden. Anwendungskonfigurationsdateien werden unter [The IDL and ACF Files (Die IDL- und ACF-Dateien) genauer erläutert.](the-idl-and-acf-files.md)

Ausführlichere Informationen zur Verwendung des MIDL-Compilers finden Sie im [Microsoft Interface Definition Language (MIDL),](/windows/desktop/Midl/midl-start-page)das Informationen zu den folgenden Themen enthält:

-   [C-Präprozessoranforderungen für MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [Überlegungen zum C/C++-Compiler](/windows/desktop/Midl/c-c-compiler-considerations)
-   [Für eine RPC-Schnittstelle generierte Dateien](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [MIDL-Befehlszeilenreferenz](/windows/desktop/Midl/midl-command-line-reference)
-   [MIDL-Sprachreferenz](/windows/desktop/Midl/midl-language-reference)
-   [MIDL-Compilerfehler und -Warnungen](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 