---
title: Verwenden von Mittel l
description: Erstellen und Kompilieren einer Microsoft Interface Definition Language-Schnittstelle (Mittel l) und eines Remote Prozedur Aufrufs (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730016"
---
# <a name="using-midl"></a>Verwenden von Mittel l

Alle Schnittstellen für Programme, die RPC verwenden, müssen in Microsoft Interface Definition Language (mittlerer l) definiert und mit dem Mittel-Compiler kompiliert werden. Die folgenden Themen bieten eine kurze Übersicht über das Erstellen und Kompilieren einer Mittel l-Schnittstelle:

-   [Definieren einer Schnittstelle mit mittlerer l](#defining-an-interface-with-midl)
-   [Kompilieren einer Mittel l-Datei](#compiling-a-midl-file)

Eine ausführliche Erläuterung dieser Themen finden Sie in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Definieren einer Schnittstelle mit mittlerer l

Bei mittlerer l-Dateien handelt es sich um Textdateien, die Sie mit einem Text-Editor erstellen und bearbeiten können. Wenn Sie eine UUID für Ihre Schnittstelle generieren, speichern Sie die Ausgabe in der Regel in einer Vorlagen-mittlerer l-Datei. Weitere Informationen zu UUIDs finden Sie unter [Erstellen von Schnittstellen-UUIDs](generating-interface-uuids.md).

Alle Schnittstellen in der mittleren l-Datei haben das gleiche Format. Sie beginnen mit einem Header, der eine Liste von Schnittstellen Attributen und den Schnittstellennamen enthält. Die Attribute werden in eckige Klammern eingeschlossen. Auf den Schnittstellen Header folgt der Text, der in geschweiften Klammern eingeschlossen ist. Im folgenden Beispiel wird eine einfache Schnittstelle angezeigt:

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

Einige der Attribute, die in der Regel in einer Mitte der Schnittstellen Definition vorkommen, sind die UUID und die Versionsnummer der-Schnittstelle. Der Text der Schnittstellen Definition muss die Prozedur Deklarationen aller Remote Prozeduren in der Schnittstelle enthalten. Sie kann auch die Deklarationen von Datentypen und Konstanten enthalten, die für die Schnittstelle erforderlich sind.

Alle Parameter in den Remote Prozedur Deklarationen müssen als " \[ [**in**](/windows/desktop/Midl/in)" \] , " \[ [**out**](/windows/desktop/Midl/out-idl)" \] oder "in" oder " \[  **out** \] " deklariert werden. Diese Deklarationen geben an, dass das Client Programm Daten an eine Remote Prozedur übergibt, dass Daten aus einer Remote Prozedur abgerufen werden oder beides. Ausführlichere Informationen zu Schnittstellenparameter Deklarationen finden Sie [im Text der IDL-Schnittstelle](the-idl-interface-body.md).

## <a name="compiling-a-midl-file"></a>Kompilieren einer Mittel l-Datei

Der Mittelwert des compl-Compilers ist ein Befehlszeilen Tool, das automatisch mit dem Platform Software Development Kit (SDK) installiert wird. Rufen Sie es in einem Befehlsfenster auf, indem Sie in der Befehlszeile den Befehl " **Mittel l**", gefolgt vom Namen einer Mittel l-Datei, eingeben. Stellen Sie sicher, dass sich das Verzeichnis mit dem Mittelwert Compiler in Ihrem Pfad befindet. Im folgenden Beispiel wird die Verwendung von veranschaulicht:

**mittlere MyApp. idl**

Beachten Sie, dass Sie die Erweiterung nicht einschließen müssen, wenn der Dateiname die Erweiterung IDL hat. Sie können auch die [Befehls Zeilenschalter](/windows/desktop/Midl/midl-command-line-reference) für den Mittelpunkt Compiler verwenden, indem Sie Sie zwischen dem Befehl " **Mittel l** " und dem Dateinamen einfügen. Dies wird im folgenden Beispiel veranschaulicht:

**Mittel l/ACF MyApp. ACF MyApp. idl**

In diesem Beispiel wird der Mittelwert Compiler mithilfe der Datei "MyApp. idl" als Eingabedatei ausgeführt. Der Befehls Zeilenschalter **/ACF** weist den Compiler an, eine Anwendungs Konfigurationsdatei (ACF) für die Eingabe zu verwenden. Anwendungs Konfigurationsdateien werden in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md)ausführlicher erläutert.

Ausführlichere Informationen zur Verwendung des-Mittell-Compilers finden Sie in der [Microsoft Interface Definition Language (Mittel l)](/windows/desktop/Midl/midl-start-page), die Informationen zu den folgenden Themen enthält:

-   [C-präprozessoranforderungen für die Mittel l](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [C/C++-compilerüberlegungen](/windows/desktop/Midl/c-c-compiler-considerations)
-   [Für eine RPC-Schnittstelle generierte Dateien](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [Referenz zur mittleren l-Befehlszeile](/windows/desktop/Midl/midl-command-line-reference)
-   [Mittel l-Sprachreferenz](/windows/desktop/Midl/midl-language-reference)
-   [Compilerfehler und-Warnungen](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 