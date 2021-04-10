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
# <a name="using-midl"></a><span data-ttu-id="eb28e-103">Verwenden von Mittel l</span><span class="sxs-lookup"><span data-stu-id="eb28e-103">Using MIDL</span></span>

<span data-ttu-id="eb28e-104">Alle Schnittstellen für Programme, die RPC verwenden, müssen in Microsoft Interface Definition Language (mittlerer l) definiert und mit dem Mittel-Compiler kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="eb28e-104">All interfaces for programs using RPC must be defined in Microsoft Interface Definition Language (MIDL) and compiled with the MIDL compiler.</span></span> <span data-ttu-id="eb28e-105">Die folgenden Themen bieten eine kurze Übersicht über das Erstellen und Kompilieren einer Mittel l-Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="eb28e-105">The following topics present a brief overview of creating and compiling a MIDL interface:</span></span>

-   [<span data-ttu-id="eb28e-106">Definieren einer Schnittstelle mit mittlerer l</span><span class="sxs-lookup"><span data-stu-id="eb28e-106">Defining an Interface with MIDL</span></span>](#defining-an-interface-with-midl)
-   [<span data-ttu-id="eb28e-107">Kompilieren einer Mittel l-Datei</span><span class="sxs-lookup"><span data-stu-id="eb28e-107">Compiling a MIDL File</span></span>](#compiling-a-midl-file)

<span data-ttu-id="eb28e-108">Eine ausführliche Erläuterung dieser Themen finden Sie in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="eb28e-108">For a detailed discussion of these topics, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

## <a name="defining-an-interface-with-midl"></a><span data-ttu-id="eb28e-109">Definieren einer Schnittstelle mit mittlerer l</span><span class="sxs-lookup"><span data-stu-id="eb28e-109">Defining an Interface with MIDL</span></span>

<span data-ttu-id="eb28e-110">Bei mittlerer l-Dateien handelt es sich um Textdateien, die Sie mit einem Text-Editor erstellen und bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="eb28e-110">MIDL files are text files that you can create and edit with a text editor.</span></span> <span data-ttu-id="eb28e-111">Wenn Sie eine UUID für Ihre Schnittstelle generieren, speichern Sie die Ausgabe in der Regel in einer Vorlagen-mittlerer l-Datei.</span><span class="sxs-lookup"><span data-stu-id="eb28e-111">If you generate a UUID for your interface, you will typically store the output in a template MIDL file.</span></span> <span data-ttu-id="eb28e-112">Weitere Informationen zu UUIDs finden Sie unter [Erstellen von Schnittstellen-UUIDs](generating-interface-uuids.md).</span><span class="sxs-lookup"><span data-stu-id="eb28e-112">For more information on UUIDs, see [Generating Interface UUIDs](generating-interface-uuids.md).</span></span>

<span data-ttu-id="eb28e-113">Alle Schnittstellen in der mittleren l-Datei haben das gleiche Format.</span><span class="sxs-lookup"><span data-stu-id="eb28e-113">All interfaces in MIDL follow the same format.</span></span> <span data-ttu-id="eb28e-114">Sie beginnen mit einem Header, der eine Liste von Schnittstellen Attributen und den Schnittstellennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="eb28e-114">They begin with a header that contains a list of interface attributes and the interface name.</span></span> <span data-ttu-id="eb28e-115">Die Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="eb28e-115">The attributes are enclosed in square brackets.</span></span> <span data-ttu-id="eb28e-116">Auf den Schnittstellen Header folgt der Text, der in geschweiften Klammern eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="eb28e-116">The interface header is followed by its body, which is enclosed in curly brackets.</span></span> <span data-ttu-id="eb28e-117">Im folgenden Beispiel wird eine einfache Schnittstelle angezeigt:</span><span class="sxs-lookup"><span data-stu-id="eb28e-117">A simple interface is shown in the following example:</span></span>

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

<span data-ttu-id="eb28e-118">Einige der Attribute, die in der Regel in einer Mitte der Schnittstellen Definition vorkommen, sind die UUID und die Versionsnummer der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eb28e-118">Some of the attributes that typically appear in a MIDL interface definition are the UUID and the interface version number.</span></span> <span data-ttu-id="eb28e-119">Der Text der Schnittstellen Definition muss die Prozedur Deklarationen aller Remote Prozeduren in der Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb28e-119">The body of the interface definition must contain the procedure declarations of all of the remote procedures in the interface.</span></span> <span data-ttu-id="eb28e-120">Sie kann auch die Deklarationen von Datentypen und Konstanten enthalten, die für die Schnittstelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eb28e-120">It can also contain the declarations of data types and constants required by the interface.</span></span>

<span data-ttu-id="eb28e-121">Alle Parameter in den Remote Prozedur Deklarationen müssen als " \[ [**in**](/windows/desktop/Midl/in)" \] , " \[ [**out**](/windows/desktop/Midl/out-idl)" \] oder "in" oder " \[  **out** \] " deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="eb28e-121">All parameters in the remote procedure declarations must be declared as \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], or \[**in**, **out**\].</span></span> <span data-ttu-id="eb28e-122">Diese Deklarationen geben an, dass das Client Programm Daten an eine Remote Prozedur übergibt, dass Daten aus einer Remote Prozedur abgerufen werden oder beides.</span><span class="sxs-lookup"><span data-stu-id="eb28e-122">These declarations specify that the client program passes data into a remote procedure, gets data out of a remote procedure, or both.</span></span> <span data-ttu-id="eb28e-123">Ausführlichere Informationen zu Schnittstellenparameter Deklarationen finden Sie [im Text der IDL-Schnittstelle](the-idl-interface-body.md).</span><span class="sxs-lookup"><span data-stu-id="eb28e-123">For more detailed information about interface parameter declarations, see [The IDL Interface Body](the-idl-interface-body.md).</span></span>

## <a name="compiling-a-midl-file"></a><span data-ttu-id="eb28e-124">Kompilieren einer Mittel l-Datei</span><span class="sxs-lookup"><span data-stu-id="eb28e-124">Compiling a MIDL File</span></span>

<span data-ttu-id="eb28e-125">Der Mittelwert des compl-Compilers ist ein Befehlszeilen Tool, das automatisch mit dem Platform Software Development Kit (SDK) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="eb28e-125">The MIDL compiler is a command-line tool that is automatically installed with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="eb28e-126">Rufen Sie es in einem Befehlsfenster auf, indem Sie in der Befehlszeile den Befehl " **Mittel l**", gefolgt vom Namen einer Mittel l-Datei, eingeben.</span><span class="sxs-lookup"><span data-stu-id="eb28e-126">Invoke it in a command window by typing the command **midl**, followed by the name of a MIDL file, at the command line.</span></span> <span data-ttu-id="eb28e-127">Stellen Sie sicher, dass sich das Verzeichnis mit dem Mittelwert Compiler in Ihrem Pfad befindet.</span><span class="sxs-lookup"><span data-stu-id="eb28e-127">Make sure that the directory containing the MIDL compiler is in your path.</span></span> <span data-ttu-id="eb28e-128">Im folgenden Beispiel wird die Verwendung von veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="eb28e-128">The following example illustrates its use:</span></span>

<span data-ttu-id="eb28e-129">**mittlere MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="eb28e-129">**midl MyApp.idl**</span></span>

<span data-ttu-id="eb28e-130">Beachten Sie, dass Sie die Erweiterung nicht einschließen müssen, wenn der Dateiname die Erweiterung IDL hat.</span><span class="sxs-lookup"><span data-stu-id="eb28e-130">Note that you do not have to include the extension if the file name has the .idl extension.</span></span> <span data-ttu-id="eb28e-131">Sie können auch die [Befehls Zeilenschalter](/windows/desktop/Midl/midl-command-line-reference) für den Mittelpunkt Compiler verwenden, indem Sie Sie zwischen dem Befehl " **Mittel l** " und dem Dateinamen einfügen.</span><span class="sxs-lookup"><span data-stu-id="eb28e-131">You can also use the MIDL compiler [command-line switches](/windows/desktop/Midl/midl-command-line-reference) by inserting them between the **midl** command and the file name.</span></span> <span data-ttu-id="eb28e-132">Dies wird im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="eb28e-132">This is demonstrated in the following example:</span></span>

<span data-ttu-id="eb28e-133">**Mittel l/ACF MyApp. ACF MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="eb28e-133">**midl /acf MyApp.acf MyApp.idl**</span></span>

<span data-ttu-id="eb28e-134">In diesem Beispiel wird der Mittelwert Compiler mithilfe der Datei "MyApp. idl" als Eingabedatei ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb28e-134">In this example, the MIDL compiler is executed using the file MyApp.idl as the input file.</span></span> <span data-ttu-id="eb28e-135">Der Befehls Zeilenschalter **/ACF** weist den Compiler an, eine Anwendungs Konfigurationsdatei (ACF) für die Eingabe zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb28e-135">The command line switch **/acf** instructs the compiler to use an application configuration file (ACF) for input as well.</span></span> <span data-ttu-id="eb28e-136">Anwendungs Konfigurationsdateien werden in [den IDL-und ACF-Dateien](the-idl-and-acf-files.md)ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="eb28e-136">Application configuration files are discussed more thoroughly in [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="eb28e-137">Ausführlichere Informationen zur Verwendung des-Mittell-Compilers finden Sie in der [Microsoft Interface Definition Language (Mittel l)](/windows/desktop/Midl/midl-start-page), die Informationen zu den folgenden Themen enthält:</span><span class="sxs-lookup"><span data-stu-id="eb28e-137">For more detailed information on using the MIDL compiler, see the [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), which contains information on the following topics:</span></span>

-   [<span data-ttu-id="eb28e-138">C-präprozessoranforderungen für die Mittel l</span><span class="sxs-lookup"><span data-stu-id="eb28e-138">C-Preprocessor Requirements for MIDL</span></span>](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [<span data-ttu-id="eb28e-139">C/C++-compilerüberlegungen</span><span class="sxs-lookup"><span data-stu-id="eb28e-139">C/C++-Compiler Considerations</span></span>](/windows/desktop/Midl/c-c-compiler-considerations)
-   [<span data-ttu-id="eb28e-140">Für eine RPC-Schnittstelle generierte Dateien</span><span class="sxs-lookup"><span data-stu-id="eb28e-140">Files Generated for an RPC Interface</span></span>](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [<span data-ttu-id="eb28e-141">Referenz zur mittleren l-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="eb28e-141">MIDL Command-line Reference</span></span>](/windows/desktop/Midl/midl-command-line-reference)
-   [<span data-ttu-id="eb28e-142">Mittel l-Sprachreferenz</span><span class="sxs-lookup"><span data-stu-id="eb28e-142">MIDL Language Reference</span></span>](/windows/desktop/Midl/midl-language-reference)
-   [<span data-ttu-id="eb28e-143">Compilerfehler und-Warnungen</span><span class="sxs-lookup"><span data-stu-id="eb28e-143">MIDL Compiler Errors and Warnings</span></span>](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 