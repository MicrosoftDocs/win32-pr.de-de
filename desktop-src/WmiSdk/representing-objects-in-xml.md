---
description: Generiert XML-Darstellungen von-Objekten.
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Darstellen von Objekten in XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9698c54eeff61517a1389ceea14bc2415727f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347321"
---
# <a name="representing-objects-in-xml"></a><span data-ttu-id="d54db-103">Darstellen von Objekten in XML</span><span class="sxs-lookup"><span data-stu-id="d54db-103">Representing Objects in XML</span></span>

<span data-ttu-id="d54db-104">Die XML-Encoderkomponente in WMI generiert XML-Darstellungen von Objekten.</span><span class="sxs-lookup"><span data-stu-id="d54db-104">The XML encoder component in WMI generates XML representations of objects.</span></span>

<span data-ttu-id="d54db-105">In C++ können Sie den XML-Encoder mit einem-Befehl für die [**iwbewbjecttextrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Methode starten, indem Sie das Objekt angeben, das in XML dargestellt werden soll, und das Textformat, das in der Darstellung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d54db-105">In C++, you can start the XML encoder with a call to the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method, specifying the object to be represented in XML and the text format to use in the representation.</span></span> <span data-ttu-id="d54db-106">Weitere Informationen und ein Codebeispiel finden Sie unter so codieren Sie ein Objekt in XML mithilfe von C/C++.</span><span class="sxs-lookup"><span data-stu-id="d54db-106">For more information and a code example, see To encode an object in XML using C/C++.</span></span>

<span data-ttu-id="d54db-107">Wenn Sie in VBScript oder Visual Basic Daten für eine XML-Instanz codieren möchten, können Sie die [**Datei "errbemubjectex. gettext**](swbemobjectex-gettext-.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d54db-107">In VBScript or Visual Basic, to encode data for an XML instance, call [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md).</span></span> <span data-ttu-id="d54db-108">Weitere Informationen und ein Codebeispiel finden Sie unter so codieren Sie ein Objekt in XML mithilfe von VBScript.</span><span class="sxs-lookup"><span data-stu-id="d54db-108">For more information and a code example, see To encode an object in XML using VBScript.</span></span>

<span data-ttu-id="d54db-109">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="d54db-109">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="d54db-110">Codieren eines Objekts mithilfe von C oder C++</span><span class="sxs-lookup"><span data-stu-id="d54db-110">Encode an Object Using C or C++</span></span>](#encode-an-object-using-c-or-c)
-   [<span data-ttu-id="d54db-111">Codieren eines Objekts mit VBScript</span><span class="sxs-lookup"><span data-stu-id="d54db-111">Encode an Object Using VBScript</span></span>](#encode-an-object-using-vbscript)
-   [<span data-ttu-id="d54db-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d54db-112">Related topics</span></span>](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a><span data-ttu-id="d54db-113">Codieren eines Objekts mithilfe von C oder C++</span><span class="sxs-lookup"><span data-stu-id="d54db-113">Encode an Object Using C or C++</span></span>

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

<span data-ttu-id="d54db-114">Im folgenden Verfahren wird beschrieben, wie Sie ein Objekt in XML mithilfe von C oder C++ codieren.</span><span class="sxs-lookup"><span data-stu-id="d54db-114">The following procedure describes how to encode an object in XML using C or C++.</span></span>

<span data-ttu-id="d54db-115">**So codieren Sie ein Objekt in XML mithilfe von C oder C++**</span><span class="sxs-lookup"><span data-stu-id="d54db-115">**To encode an object in XML using C or C++**</span></span>

1.  <span data-ttu-id="d54db-116">Richten Sie Ihr Programm für den Zugriff auf WMI-Daten ein.</span><span class="sxs-lookup"><span data-stu-id="d54db-116">Set up your program to access WMI data.</span></span>

    <span data-ttu-id="d54db-117">Da WMI auf der com-Technologie basiert, müssen Sie die erforderlichen Aufrufe an die Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ausführen, um auf WMI zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d54db-117">Because WMI is based on COM technology, you must perform the requisite calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span> <span data-ttu-id="d54db-118">Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="d54db-118">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="d54db-119">Erstellen Sie optional ein [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt, und initialisieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="d54db-119">Optionally, create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object and initialize it.</span></span>

    <span data-ttu-id="d54db-120">Sie müssen das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt nur erstellen, wenn Sie den Standard Vorgang ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="d54db-120">You do not need to create the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object unless you need to change the default operation.</span></span> <span data-ttu-id="d54db-121">Das Context-Objekt wird vom XML-Encoder zum Steuern der Menge der Informationen verwendet, die in der XML-Darstellung des Objekts enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d54db-121">The context object is used by the XML encoder to control the amount of information included in the object's XML representation.</span></span>

    <span data-ttu-id="d54db-122">In der folgenden Tabelle werden die optionalen Werte aufgelistet, die für das Kontext Objekt angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="d54db-122">The following table lists the optional values that can be specified for the context object.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d54db-123">Wert/Typ</span><span class="sxs-lookup"><span data-stu-id="d54db-123">Value/type</span></span></th>
    <th><span data-ttu-id="d54db-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d54db-124">Meaning</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d54db-125">&quot;LocalOnly- &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d54db-125">&quot;LocalOnly&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="d54db-126">Wenn <strong>true</strong>, sind nur Eigenschaften und Methoden, die lokal in der-Klasse definiert sind, im resultierenden XML-Code vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d54db-126">When <strong>TRUE</strong>, only properties and methods defined locally in the class are present in the resulting XML.</span></span> <span data-ttu-id="d54db-127">Der Standardwert ist <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="d54db-127">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d54db-128">&quot;Includecoqualifizierer &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d54db-128">&quot;IncludeQualifiers&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="d54db-129">Wenn <strong>true</strong>, sind die Qualifizierer Class, instance, Properties und Method im resultierenden XML-Code enthalten.</span><span class="sxs-lookup"><span data-stu-id="d54db-129">When <strong>TRUE</strong>, class, instance, properties, and method qualifiers are included in the resulting XML.</span></span> <span data-ttu-id="d54db-130">Der Standardwert ist <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="d54db-130">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d54db-131">&quot;Excludebug SystemProperties- &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d54db-131">&quot;ExcludeSystemProperties&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="d54db-132"><strong>True</strong>gibt an, dass die WMI-Systemeigenschaften aus der Ausgabe herausgefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="d54db-132">When <strong>TRUE</strong>, WMI system properties are filtered out of the output.</span></span> <span data-ttu-id="d54db-133">Der Standardwert ist <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="d54db-133">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d54db-134">&quot;Pathlevel- &quot; <strong>VT_I4</strong></span><span class="sxs-lookup"><span data-stu-id="d54db-134">&quot;PathLevel&quot; <strong>VT_I4</strong></span></span></td>
    <td><dl> <span data-ttu-id="d54db-135">0 = ein- <CLASS> oder- <INSTANCE> Element wird generiert.</span><span class="sxs-lookup"><span data-stu-id="d54db-135">0 = A <CLASS> or <INSTANCE> element is generated.</span></span><br />
<span data-ttu-id="d54db-136">1 = ein- <VALUE.NAMEDOBJECT> Element wird generiert.</span><span class="sxs-lookup"><span data-stu-id="d54db-136">1 = A <VALUE.NAMEDOBJECT> element is generated.</span></span><br />
<span data-ttu-id="d54db-137">2 = ein- <VALUE.OBJECTWITHLOCALPATH> Element wird generiert.</span><span class="sxs-lookup"><span data-stu-id="d54db-137">2 = A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span><br />
<span data-ttu-id="d54db-138">3 = eine <VALUE.OBJECTWITHPATH> wird generiert.</span><span class="sxs-lookup"><span data-stu-id="d54db-138">3 = A <VALUE.OBJECTWITHPATH> is generated.</span></span><br />
    </dl> <span data-ttu-id="d54db-139">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d54db-139">The default is 0 (zero).</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

    <span data-ttu-id="d54db-140">Das folgende Codebeispiel zeigt, wie das Kontext Objekt initialisiert wird, um Qualifizierer einzuschließen und Systemeigenschaften auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="d54db-140">The following code example shows how the context object is initialized to include qualifiers and exclude system properties.</span></span>

    ```C++
    VARIANT vValue;
    IWbemContext *pContext = NULL;
    HRESULT hr = CoCreateInstance (CLSID_WbemContext, 
                           NULL, 
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemContext, 
                           (void**) &pContext);
    if (FAILED(hr))
    {
      printf("Create context failed with %x\n", hr);
      return hr;
    }

    // Generate a <VALUE.OBJECTWITHLOCALPATH> element
    VariantInit(&vValue);
    vValue.vt = VT_I4;
    vValue.lVal = 2;
    pContext->SetValue(L"PathLevel", 0, &vValue);
    VariantClear(&vValue);

    // Include qualifiers
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
    VariantClear(&vValue);

    // Exclude system properties
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
    VariantClear(&vValue);
    ```

    

3.  <span data-ttu-id="d54db-141">Sie erhalten einen Verweis auf die-Klasse oder-Instanz, um Sie in XML zu codieren.</span><span class="sxs-lookup"><span data-stu-id="d54db-141">Get a reference to the class or instance to encode in XML.</span></span>

    <span data-ttu-id="d54db-142">Nachdem Sie com initialisiert und mit WMI verbunden sind, rufen Sie [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) auf, um einen Verweis auf die angegebene Klasse oder Instanz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d54db-142">After you have initialized COM and are connected to WMI, call [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a reference to the specified class or instance.</span></span> <span data-ttu-id="d54db-143">Wenn Sie einen BSTR verwendet haben, um die Klasse oder Instanz anzugeben, nennen Sie [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) , um den von [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)belegten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d54db-143">If you used a BSTR to specify the class or instance, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free up the memory allocated by [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span>

    <span data-ttu-id="d54db-144">Im folgenden Codebeispiel wird ein Verweis auf eine [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d54db-144">The following code example retrieves a reference to an [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance.</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemClassObject *pClass = NULL;
    BSTR strObj = SysAllocString(L"Win32_LogicalDisk");

    hr = pConnection->GetObject(strObj, 
                                0, 
                                NULL, 
                                &pClass, 
                                NULL);

    SysFreeString(strObj);
    if (FAILED(hr))
    {
      printf("GetObject failed with %x\n",hr)
      return hr;
    }
    ```

    

4.  <span data-ttu-id="d54db-145">Erstellen Sie ein [**iwbejebjecttextrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d54db-145">Create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object.</span></span>

    <span data-ttu-id="d54db-146">Nachdem Sie einen Verweis auf ein Objekt erstellt haben, müssen Sie das Objekt " [**iwbepfad**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) " mit einem [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)-Befehl erstellen.</span><span class="sxs-lookup"><span data-stu-id="d54db-146">After you have a reference to an object you must create the [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="d54db-147">Das Objekt " **iwbemubjecttexzrc** " wird verwendet, um den eigentlichen XML-Text zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d54db-147">The **IWbemObjectTextSrc** object is used to generate the actual XML text.</span></span>

    <span data-ttu-id="d54db-148">Im folgenden Codebeispiel wird veranschaulicht, wie ein [**iwbemubjecttextrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) -Objekt durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d54db-148">The following code example shows how to create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemObjectTextSrc *pSrc = NULL;

    hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemObjectTextSrc, 
                           (void**) &pSrc);

    if (FAILED(hr))
    {
        printf("CoCreateInstance of IWbemObjectTextSrc failed %x\n",hr);
        return hr;
    }
    ```

    

5.  <span data-ttu-id="d54db-149">Rufen Sie die [**iwbewbjecttexzrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Methode auf, um eine XML-Darstellung eines Objekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d54db-149">Invoke the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method to get an XML representation of an object.</span></span>

    <span data-ttu-id="d54db-150">Nachdem Sie den Kontext für die Objektdarstellung, Abrufen eines Verweises auf das Objekt und Erstellen eines [**iwbemubjecttextrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) -Objekts festgelegt haben, können Sie eine XML-Darstellung des angegebenen Objekts generieren, indem Sie die [**iwbewbjecttextrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d54db-150">After setting the context for the object's representation, getting a reference to the object, and creating an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object, you are ready to generate an XML representation of the specified object by calling the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method.</span></span>

    <span data-ttu-id="d54db-151">Der folgende C++-Beispielcode generiert eine XML-Darstellung des Objekts, auf das von *pClass* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d54db-151">The following C++ example code generates an XML representation of the object referenced by *pClass*.</span></span> <span data-ttu-id="d54db-152">Die XML-Darstellung wird in " *strintext*" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d54db-152">The XML representation is returned in *strText*.</span></span> <span data-ttu-id="d54db-153">Der dritte Parameter von [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) gibt das Textformat an, das für den XML-Code verwendet werden soll, und muss entweder WMI \_ obj \_ Text \_ CIM \_ DTD \_ 2 \_ 0 (0x1) oder WMI \_ obj \_ Text \_ WMI \_ DTD \_ 2 \_ 0 (0x2) sein.</span><span class="sxs-lookup"><span data-stu-id="d54db-153">The third parameter of [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifies the text format to be used for the XML and must be either WMI\_OBJ\_TEXT\_CIM\_DTD\_2\_0 (0x1) or WMI\_OBJ\_TEXT\_WMI\_DTD\_2\_0 (0x2).</span></span> <span data-ttu-id="d54db-154">Weitere Informationen zu diesen Werten finden Sie unter [**iwbemubjecttextrc:: gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Parameter Werte.</span><span class="sxs-lookup"><span data-stu-id="d54db-154">For more information about these values, see [**IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.</span></span>

    ```C++
    HRESULT hr = NULL;
    BSTR strText = NULL;
    hr = pSrc->GetText(0, 
                       pClass, 
                       WMI_OBJ_TEXT_CIM_DTD_2_0,
                       pContext, 
                       &strText);

    // Perform a task with strText
    SysFreeString(strText);

    if (FAILED(hr))
    {
      printf("GetText failed with %x\n", hr);
      return hr;
    }
    ```

    

<span data-ttu-id="d54db-155">Der folgende C++-Beispielcode enthält alle Schritte in der vorherigen Prozedur und codiert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse in XML, einschließlich Klassen-, Eigenschafts-und Methoden Qualifizierern und ohne Systemeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d54db-155">The following C++ example code includes all of the steps in the previous procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML including class, property, and method qualifiers and excluding system properties.</span></span>


```C++
// The following #define statement is needed so that 
// the proper values are loaded by the #include files.
#define _WIN32_WINNT 0x0500

#include <stdio.h>
#include <wbemcli.h>
#pragma comment(lib, "wbemuuid.lib")

// Initialize the context object
// ---------------------------------------------
void FillUpContext(IWbemContext *pContext)
{
  VARIANT vValue;

  // IncludeQualifiers
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_FALSE;
  pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
  VariantClear(&vValue);

  VariantInit(&vValue);
  vValue.vt = VT_I4;
  vValue.lVal = 0;
  pContext->SetValue(L"PathLevel", 0, &vValue);
  VariantClear(&vValue);

  // ExcludeSystemProperties
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_TRUE;
  pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
  VariantClear(&vValue);
}

// Main method ... drives the program
// ---------------------------------------------
int _cdecl main(int argc, char * argv[])
{
  BSTR strNs = NULL;
  BSTR strObj = NULL;
  BSTR strText = NULL;

  if(FAILED(CoInitialize(NULL)))
    return 1;
  HRESULT hr = E_FAIL;
  IWbemObjectTextSrc *pSrc = NULL;

  IWbemLocator *pL = NULL;
  if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemLocator, 
                                      NULL, 
                                      CLSCTX_INPROC_SERVER,
                                      IID_IWbemLocator, 
                                      (void**) &pL)))
  {
    // Create a context object
    IWbemContext *pContext = NULL;
    if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemContext, 
                                        NULL, 
                                        CLSCTX_INPROC_SERVER,
                                        IID_IWbemContext, 
                                        (void**) &pContext)))
    {
      FillUpContext(pContext);
      IWbemServices *pConnection = NULL;
      strNs = SysAllocString(L"root\\cimv2");
      strText = NULL;
      if(SUCCEEDED(hr = pL->ConnectServer(strNs, 
                                          NULL, 
                                          NULL, 
                                          NULL, 
                                          0, 
                                          NULL, 
                                          NULL, 
                                          &pConnection)))
      {
        IWbemClassObject *pClass = NULL;
        strObj = SysAllocString(L"Win32_LogicalDisk");

        if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                                            NULL,
                                            CLSCTX_INPROC_SERVER,
                                            IID_IWbemObjectTextSrc, 
                                            (void**) &pSrc)))
        {
          // Test for GetObject
          if(SUCCEEDED(hr = pConnection->GetObject(strObj, 
                                                   0, 
                                                   NULL, 
                                                   &pClass, 
                                                   NULL)))
          {
            if(SUCCEEDED(hr = pSrc->GetText(0, 
                                            pClass, 
                                            WMI_OBJ_TEXT_CIM_DTD_2_0,
                                            pContext, 
                                            &strText)))
            {
              printf("GETOBJECT SUCCEEDED\n");
              printf("==========================================\n");
              wprintf(strText);
              pContext->Release();
              pClass->Release();
            }
            else
            {
              printf("GetText failed with %x\n", hr);
              // Free up the object
              pContext->Release();
              pClass->Release();
            }
          }
          else
            printf("GetObject failed with %x\n", hr);
        }
        else
          printf("CoCreateInstance on WbemObjectTextSrc failed with %x\n", hr);
      }
      else
        printf("ConnectServer on root\\cimv2 failed with %x\n", hr);
    }
    else
      printf("CoCreateInstance on Context failed with %x\n", hr);
  }
  else
    printf("CoCreateInstance on Locator failed with %x\n", hr);

// Clean up memory
  if (strNs != NULL)
    SysFreeString(strNs);
  if (strObj != NULL)
    SysFreeString(strObj);
  if (strText != NULL)
    SysFreeString(strText);
  if (pSrc != NULL)
    pSrc->Release();
  if (pL != NULL)
    pL->Release();
  return 0;
}
```



## <a name="encode-an-object-using-vbscript"></a><span data-ttu-id="d54db-156">Codieren eines Objekts mit VBScript</span><span class="sxs-lookup"><span data-stu-id="d54db-156">Encode an Object Using VBScript</span></span>

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

<span data-ttu-id="d54db-157">Im folgenden Verfahren wird beschrieben, wie Sie ein Objekt in XML mithilfe von VBScript codieren.</span><span class="sxs-lookup"><span data-stu-id="d54db-157">The following procedure describes how to encode an object in XML using VBScript.</span></span>

<span data-ttu-id="d54db-158">**So codieren Sie ein Objekt in XML mithilfe von VBScript**</span><span class="sxs-lookup"><span data-stu-id="d54db-158">**To encode an object in XML using VBScript**</span></span>

1.  <span data-ttu-id="d54db-159">Erstellen Sie optional ein Objekt " [**austauenamedvalueset**](swbemnamedvalueset.md) ", und initialisieren Sie es, um die für die XML-Darstellung erforderlichen Kontext Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d54db-159">Optionally, create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object and initialize it so as to set the context values required for the XML representation.</span></span>

    <span data-ttu-id="d54db-160">Im folgenden Codebeispiel wird gezeigt, wie die-Werte den XML-Encoder anweisen, einen <Wert zu generieren. Objectwithlocalpath>-Element, einschließlich aller Qualifizierer und ausgenommen Systemeigenschaften beim Konstruieren der XML-Darstellung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d54db-160">The following code example shows how the values instruct the XML encoder to generate a <VALUE.OBJECTWITHLOCALPATH> element, including all of the qualifiers and excluding system properties when it constructs the XML representation of the object.</span></span>

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  <span data-ttu-id="d54db-161">Rufen Sie eine Instanz des Objekts oder der Klasse ab, die in XML dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d54db-161">Retrieve an instance of the object or class to represent in XML.</span></span>

    <span data-ttu-id="d54db-162">Im folgenden Codebeispiel wird eine Instanz des-Objekts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d54db-162">The following code example retrieves an instance of the object.</span></span>

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  <span data-ttu-id="d54db-163">Rufen Sie die [**gettext \_**](swbemobjectex-gettext-.md) -Methode der-Instanz auf, die Sie im vorherigen Schritt erstellt haben, und verwenden Sie dabei 1 als Parameter, um das Textformat anzugeben, das CIM DTD Version 2,0 entspricht, oder 2, um das Textformat anzugeben, das WMI DTD Version 2,0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="d54db-163">Invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance created in the preceding step, using 1 as the parameter to specify the text format that corresponds to CIM DTD version 2.0, or 2 to specify the text format that corresponds to WMI DTD version 2.0.</span></span> <span data-ttu-id="d54db-164">Wenn Sie das Objekt " [**slibemnamedvalueset**](swbemnamedvalueset.md) " in Schritt 1 erstellt haben, fügen Sie es in der Parameterliste als dritten Parameter ein.</span><span class="sxs-lookup"><span data-stu-id="d54db-164">If you created the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object in Step 1, include it in the parameter list as the third parameter.</span></span>

    <span data-ttu-id="d54db-165">Im folgenden Codebeispiel wird gezeigt, wie die [**gettext \_**](swbemobjectex-gettext-.md) -Methode der-Instanz aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d54db-165">The following code example shows how to invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance.</span></span>

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  <span data-ttu-id="d54db-166">Optional können Sie überprüfen, ob es sich bei dem in Schritt 3 generierten XML-Code um wohl geformtes XML handelt, indem Sie ein XML-Dokumentobjektmodell (DOM)-Objekt erstellen und initialisieren und dann den XML-Text darin laden.</span><span class="sxs-lookup"><span data-stu-id="d54db-166">Optionally, validate that the XML generated in Step 3 is well-formed XML, by creating and initializing an XML Document Object Model (DOM) object and then load the XML text into it.</span></span>

    <span data-ttu-id="d54db-167">Im folgenden Codebeispiel wird gezeigt, wie ein XML-DOM-Objekt erstellt und initialisiert und der XML-Text in dieses Objekt geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d54db-167">The following code example shows how to create and initialize an XML DOM object and load the XML text into it.</span></span>

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  <span data-ttu-id="d54db-168">Gibt die XML-Darstellung des-Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="d54db-168">Output the XML representation of the object.</span></span>

    <span data-ttu-id="d54db-169">Im folgenden Codebeispiel wird gezeigt, wie WScript verwendet wird, um den XML-Code auszugeben.</span><span class="sxs-lookup"><span data-stu-id="d54db-169">The following code example shows how to use wscript to output the XML.</span></span>

    ```VB
    wscript.echo strText
    ```

    

    <span data-ttu-id="d54db-170">Wenn Sie sich entschieden haben, das XML-DOM zu verwenden, um zu überprüfen, ob der generierte XML-Code wohl geformt ist, ersetzen Sie die vorherige Zeile durch Folgendes</span><span class="sxs-lookup"><span data-stu-id="d54db-170">If you chose to use XML DOM to verify that the XML generated is well-formed, replace the previous line with the following.</span></span>

    ```VB
    wscript.echo xml.xml
    ```

    

<span data-ttu-id="d54db-171">Das folgende VBScript-Codebeispiel enthält alle Schritte in der vorherigen Prozedur und codiert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse in XML, einschließlich der Klassen-, Eigenschaften-und Methoden Qualifizierer und ausgenommen der Systemeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d54db-171">The following VBScript code example includes all of the steps in the preceding procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML, including class, property, and method qualifiers and excluding system properties.</span></span>


```VB
' Create optional SWbemNamedValueSet object
set context = CreateObject("Wbemscripting.SWbemNamedValueSet")

' Initialize the context object
context.add "PathLevel", 2
context.add "IncludeQualifiers", true
context.add "ExcludeSystemProperties", true

' Retrieve the object/class to be represented in XML
set myObj = GetObject("winmgmts:\\.\root\cimv2:Win32_LogicalDisk")

' Get the XML representation of the object
strText = myObj.GetText_(2,,context)
' If you have not used a SWbemNamedValueSet object 
'   use the following line
'   strText = myObj.GetText(2)

' Print the XML representation
wscript.echo strText

' If you choose to use the XML DOM to verify 
'   that the XML generated is well-formed, replace the last
'   line in the above code example with the following lines:

' Create an XMLDOM object
set xml = CreateObject("Microsoft.xmldom")

' Initialize the XMLDOM object so results are 
'   returned synchronously
xml.async = false

' Load the XML into the XMLDOM object
xml.loadxml strText

' Print the XML representation
wscript.echo xml.xml
```



## <a name="related-topics"></a><span data-ttu-id="d54db-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d54db-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d54db-173">Verwenden von WMI</span><span class="sxs-lookup"><span data-stu-id="d54db-173">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

