---
title: Programmieren von ADSI mit Java/com
description: Mithilfe des Microsoft Virtual Machine for Java (Microsoft VM) und des Microsoft Java-Compilers haben Sie Zugriff auf alle ADSI-Features, die über alle ADSI COM-Komponenten aus einer Java/COM-Anwendung verfügbar gemacht werden.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmieren von ADSI mit Java/com AD
- ADSI ADSI, using, Java/COM-Programmierung für
- ADSI ADSI, Beispielcode Java
- ADSI ADSI, Beispielcode-Java, binden an ein ADSI-Objekt und Aufrufen von Methoden für dieses Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855267"
---
# <a name="programming-adsi-with-javacom"></a><span data-ttu-id="61225-107">Programmieren von ADSI mit Java/com</span><span class="sxs-lookup"><span data-stu-id="61225-107">Programming ADSI with Java/COM</span></span>

<span data-ttu-id="61225-108">Mithilfe des Microsoft Virtual Machine for Java (Microsoft VM) und des Microsoft Java-Compilers haben Sie Zugriff auf alle ADSI-Features, die über alle ADSI COM-Komponenten aus einer Java/COM-Anwendung verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="61225-108">Using the Microsoft virtual machine for Java (Microsoft VM) and Microsoft Java Compiler, you have access to all the ADSI features exposed through any ADSI COM components, from a Java/COM application.</span></span> <span data-ttu-id="61225-109">Das folgende Java-Codebeispiel zeigt die Elemente, die zum Binden an ein ADSI-Objekt und zum Aufrufen von Methoden für dieses Objekt erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="61225-109">The following Java code example shows the elements necessary to bind to an ADSI object and invoke methods on that object.</span></span> <span data-ttu-id="61225-110">Die erforderlichen ADSI-API-Funktionen und-Objektmethoden werden über Activeds.dll verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="61225-110">The required ADSI API functions and object methods are exposed through Activeds.dll.</span></span>


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



<span data-ttu-id="61225-111">Das-Argument in der ersten **Import** Anweisung bezieht sich auf Java-Wrapper Klassen, die in Activeds.dll verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="61225-111">The argument in the first **import** statement refers to Java Wrapper classes packaged in Activeds.dll.</span></span> <span data-ttu-id="61225-112">Verwenden Sie Visual J++, um die Wrapper Klassen zu erstellen, und fügen Sie Sie in Ihr Projekt ein, indem Sie das folgende Verfahren ausführen.</span><span class="sxs-lookup"><span data-stu-id="61225-112">Use Visual J++ to create the wrapper classes and include them in your project, following the procedure below.</span></span>

<span data-ttu-id="61225-113">**So erstellen Sie Wrapper Klassen und fügen Sie in Ihr Projekt ein**</span><span class="sxs-lookup"><span data-stu-id="61225-113">**To create wrapper classes and include them in your project**</span></span>

1.  <span data-ttu-id="61225-114">Wählen Sie in einem Visual J++-Projekt im Menü **Projekt** den Befehl **com-Wrapper hinzufügen...** aus.</span><span class="sxs-lookup"><span data-stu-id="61225-114">In a Visual J++ project, select **Add Com Wrapper...** from the **Project** menu.</span></span>
2.  <span data-ttu-id="61225-115">Wählen Sie "Active DS-Typbibliothek" aus den **installierten Komponenten aus:** im Dialogfeld COM-Wrapper.</span><span class="sxs-lookup"><span data-stu-id="61225-115">Select "Active DS Type Library" from the **Installed Components:** from the COM Wrappers dialog.</span></span> <span data-ttu-id="61225-116">Wenn die Typbibliothek nicht im Listenfeld angezeigt wird, klicken Sie auf die Schaltfläche **Durchsuchen...** , navigieren Sie zu dem Verzeichnis, in dem activeds. tlb gespeichert ist, und wählen Sie dann die Typbibliothek aus.</span><span class="sxs-lookup"><span data-stu-id="61225-116">If the type library is not shown in the list box, click the **Browse...** button, navigate to the directory where Activeds.tlb is stored, and then select the type library.</span></span>

<span data-ttu-id="61225-117">Visual J++ erstellt das activeds-Paket für die Java-Wrapper Klassen und schließt das Paket in den Standardpfad des Projekts ein.</span><span class="sxs-lookup"><span data-stu-id="61225-117">Visual J++ creates the activeds package for the Java Wrapper classes and include the package into the project's default path.</span></span> <span data-ttu-id="61225-118">Weitere Informationen finden Sie im activeds-Paket im Bereich " **Projekt durchsuchen** " im Fenster "Visual J++".</span><span class="sxs-lookup"><span data-stu-id="61225-118">For more information, see the activeds package in the **Project Explore** pane on the Visual J++ window.</span></span>

<span data-ttu-id="61225-119">Um ein ADSI-Objekt zu erhalten, das nicht coerstellt werden kann, verwenden Sie eine der verfügbar gemachten ADSI-API-Funktionen, z. b. [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), die ebenfalls in Activeds.dll verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="61225-119">To get an ADSI object that cannot be cocreated, use one of the exposed ADSI API functions, for example, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), which are also packaged in Activeds.dll.</span></span> <span data-ttu-id="61225-120">Microsoft J/Direct ermöglicht den Zugriff auf diese und andere Native APIs.</span><span class="sxs-lookup"><span data-stu-id="61225-120">Microsoft J/Direct provides access to these and other native APIs.</span></span> <span data-ttu-id="61225-121">Dies wird in den letzten beiden Zeilen des obigen Code Beispiels veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="61225-121">This is illustrated by the last two lines of the code example, above.</span></span>

<span data-ttu-id="61225-122">Stellen Sie beim Kompilieren sicher, dass die Microsoft-Spracherweiterung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="61225-122">When compiling, ensure that Microsoft Language Extension is enabled.</span></span> <span data-ttu-id="61225-123">Wählen Sie hierzu im Projektfenster von Visual J++ im Menü **Projekt** die Option **<project> Eigenschaften...** aus.</span><span class="sxs-lookup"><span data-stu-id="61225-123">To do this, select **<project> Properties...** from the **Project** menu in the Visual J++ project window.</span></span> <span data-ttu-id="61225-124">Klicken Sie dann im Dialogfeld **<project> Eigenschaften** auf die Registerkarte **Kompilieren** .</span><span class="sxs-lookup"><span data-stu-id="61225-124">Then, click the **Compile** tab in the **<project> Properties** dialog.</span></span> <span data-ttu-id="61225-125">Deaktivieren Sie das Kontrollkästchen **Microsoft-Spracherweiterungen deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="61225-125">Clear the **Disable Microsoft Language Extensions** check box.</span></span> <span data-ttu-id="61225-126">Wenn Sie in der Befehlszeile kompilieren, verwenden Sie den Schalter "/x-", z. b.:</span><span class="sxs-lookup"><span data-stu-id="61225-126">If compiling from the command line, use "/x-" switch, for example:</span></span>

<span data-ttu-id="61225-127">**JVC/x-simpleadsi. Java**</span><span class="sxs-lookup"><span data-stu-id="61225-127">**jvc /x- SimpleADSI.java**</span></span>

<span data-ttu-id="61225-128">Schließlich muss die Dynamic Link Library (dll) im Systempfad sichtbar sein, damit die virtuelle Maschine die COM-Komponente lädt.</span><span class="sxs-lookup"><span data-stu-id="61225-128">Finally, in order for the virtual machine to load the COM component, the dynamic-link library (DLL) must be visible on the system path.</span></span> <span data-ttu-id="61225-129">Wenn ein Fehler "java. lang. unbefriefedlinkerror" zurückgegeben wird, legen Sie den Pfad so fest, dass er den Pfad enthält, der die erforderliche DLL enthält.</span><span class="sxs-lookup"><span data-stu-id="61225-129">If a "java.lang.UnsatisfiedLinkError" error is returned, set the PATH to include the path that contains the required DLL.</span></span> <span data-ttu-id="61225-130">Wenn Activeds.dll z. b. in c: \\ ADSI lib installiert wurde \\ , geben Sie den folgenden Befehl über die Befehlszeile aus:</span><span class="sxs-lookup"><span data-stu-id="61225-130">For example, if Activeds.dll has been installed in c:\\adsi\\lib, issue the following command from the command line:</span></span>

<span data-ttu-id="61225-131">**set path =% path%; c: \\ ADSI \\ lib**</span><span class="sxs-lookup"><span data-stu-id="61225-131">**set PATH = %PATH%; c:\\adsi\\lib**</span></span>

 

 




