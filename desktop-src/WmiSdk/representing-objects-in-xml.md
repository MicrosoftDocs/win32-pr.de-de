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
# <a name="representing-objects-in-xml"></a>Darstellen von Objekten in XML

Die XML-Encoderkomponente in WMI generiert XML-Darstellungen von Objekten.

In C++ können Sie den XML-Encoder mit einem-Befehl für die [**iwbewbjecttextrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Methode starten, indem Sie das Objekt angeben, das in XML dargestellt werden soll, und das Textformat, das in der Darstellung verwendet werden soll. Weitere Informationen und ein Codebeispiel finden Sie unter so codieren Sie ein Objekt in XML mithilfe von C/C++.

Wenn Sie in VBScript oder Visual Basic Daten für eine XML-Instanz codieren möchten, können Sie die [**Datei "errbemubjectex. gettext**](swbemobjectex-gettext-.md)" aufrufen. Weitere Informationen und ein Codebeispiel finden Sie unter so codieren Sie ein Objekt in XML mithilfe von VBScript.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Codieren eines Objekts mithilfe von C oder C++](#encode-an-object-using-c-or-c)
-   [Codieren eines Objekts mit VBScript](#encode-an-object-using-vbscript)
-   [Zugehörige Themen](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Codieren eines Objekts mithilfe von C oder C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

Im folgenden Verfahren wird beschrieben, wie Sie ein Objekt in XML mithilfe von C oder C++ codieren.

**So codieren Sie ein Objekt in XML mithilfe von C oder C++**

1.  Richten Sie Ihr Programm für den Zugriff auf WMI-Daten ein.

    Da WMI auf der com-Technologie basiert, müssen Sie die erforderlichen Aufrufe an die Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ausführen, um auf WMI zuzugreifen. Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).

2.  Erstellen Sie optional ein [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt, und initialisieren Sie es.

    Sie müssen das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt nur erstellen, wenn Sie den Standard Vorgang ändern müssen. Das Context-Objekt wird vom XML-Encoder zum Steuern der Menge der Informationen verwendet, die in der XML-Darstellung des Objekts enthalten sind.

    In der folgenden Tabelle werden die optionalen Werte aufgelistet, die für das Kontext Objekt angegeben werden können.

    

    <table>
    <thead>
    <tr class="header">
    <th>Wert/Typ</th>
    <th>Bedeutung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;LocalOnly- &quot; <strong>VT_BOOL</strong></td>
    <td>Wenn <strong>true</strong>, sind nur Eigenschaften und Methoden, die lokal in der-Klasse definiert sind, im resultierenden XML-Code vorhanden. Der Standardwert ist <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;Includecoqualifizierer &quot; <strong>VT_BOOL</strong></td>
    <td>Wenn <strong>true</strong>, sind die Qualifizierer Class, instance, Properties und Method im resultierenden XML-Code enthalten. Der Standardwert ist <strong>FALSE</strong>.</td>
    </tr>
    <tr class="odd">
    <td>&quot;Excludebug SystemProperties- &quot; <strong>VT_BOOL</strong></td>
    <td><strong>True</strong>gibt an, dass die WMI-Systemeigenschaften aus der Ausgabe herausgefiltert werden. Der Standardwert ist <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;Pathlevel- &quot; <strong>VT_I4</strong></td>
    <td><dl> 0 = ein- <CLASS> oder- <INSTANCE> Element wird generiert.<br />
1 = ein- <VALUE.NAMEDOBJECT> Element wird generiert.<br />
2 = ein- <VALUE.OBJECTWITHLOCALPATH> Element wird generiert.<br />
3 = eine <VALUE.OBJECTWITHPATH> wird generiert.<br />
    </dl> Der Standardwert ist 0 (null).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    Das folgende Codebeispiel zeigt, wie das Kontext Objekt initialisiert wird, um Qualifizierer einzuschließen und Systemeigenschaften auszuschließen.

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

    

3.  Sie erhalten einen Verweis auf die-Klasse oder-Instanz, um Sie in XML zu codieren.

    Nachdem Sie com initialisiert und mit WMI verbunden sind, rufen Sie [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) auf, um einen Verweis auf die angegebene Klasse oder Instanz abzurufen. Wenn Sie einen BSTR verwendet haben, um die Klasse oder Instanz anzugeben, nennen Sie [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) , um den von [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)belegten Arbeitsspeicher freizugeben.

    Im folgenden Codebeispiel wird ein Verweis auf eine [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanz abgerufen.

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

    

4.  Erstellen Sie ein [**iwbejebjecttextrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) -Objekt.

    Nachdem Sie einen Verweis auf ein Objekt erstellt haben, müssen Sie das Objekt " [**iwbepfad**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) " mit einem [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)-Befehl erstellen. Das Objekt " **iwbemubjecttexzrc** " wird verwendet, um den eigentlichen XML-Text zu generieren.

    Im folgenden Codebeispiel wird veranschaulicht, wie ein [**iwbemubjecttextrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) -Objekt durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellt wird.

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

    

5.  Rufen Sie die [**iwbewbjecttexzrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Methode auf, um eine XML-Darstellung eines Objekts zu erhalten.

    Nachdem Sie den Kontext für die Objektdarstellung, Abrufen eines Verweises auf das Objekt und Erstellen eines [**iwbemubjecttextrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) -Objekts festgelegt haben, können Sie eine XML-Darstellung des angegebenen Objekts generieren, indem Sie die [**iwbewbjecttextrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Methode aufrufen.

    Der folgende C++-Beispielcode generiert eine XML-Darstellung des Objekts, auf das von *pClass* verwiesen wird. Die XML-Darstellung wird in " *strintext*" zurückgegeben. Der dritte Parameter von [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) gibt das Textformat an, das für den XML-Code verwendet werden soll, und muss entweder WMI \_ obj \_ Text \_ CIM \_ DTD \_ 2 \_ 0 (0x1) oder WMI \_ obj \_ Text \_ WMI \_ DTD \_ 2 \_ 0 (0x2) sein. Weitere Informationen zu diesen Werten finden Sie unter [**iwbemubjecttextrc:: gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) -Parameter Werte.

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

    

Der folgende C++-Beispielcode enthält alle Schritte in der vorherigen Prozedur und codiert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse in XML, einschließlich Klassen-, Eigenschafts-und Methoden Qualifizierern und ohne Systemeigenschaften.


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



## <a name="encode-an-object-using-vbscript"></a>Codieren eines Objekts mit VBScript

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

Im folgenden Verfahren wird beschrieben, wie Sie ein Objekt in XML mithilfe von VBScript codieren.

**So codieren Sie ein Objekt in XML mithilfe von VBScript**

1.  Erstellen Sie optional ein Objekt " [**austauenamedvalueset**](swbemnamedvalueset.md) ", und initialisieren Sie es, um die für die XML-Darstellung erforderlichen Kontext Werte festzulegen.

    Im folgenden Codebeispiel wird gezeigt, wie die-Werte den XML-Encoder anweisen, einen <Wert zu generieren. Objectwithlocalpath>-Element, einschließlich aller Qualifizierer und ausgenommen Systemeigenschaften beim Konstruieren der XML-Darstellung des Objekts.

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  Rufen Sie eine Instanz des Objekts oder der Klasse ab, die in XML dargestellt werden soll.

    Im folgenden Codebeispiel wird eine Instanz des-Objekts abgerufen.

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Rufen Sie die [**gettext \_**](swbemobjectex-gettext-.md) -Methode der-Instanz auf, die Sie im vorherigen Schritt erstellt haben, und verwenden Sie dabei 1 als Parameter, um das Textformat anzugeben, das CIM DTD Version 2,0 entspricht, oder 2, um das Textformat anzugeben, das WMI DTD Version 2,0 entspricht. Wenn Sie das Objekt " [**slibemnamedvalueset**](swbemnamedvalueset.md) " in Schritt 1 erstellt haben, fügen Sie es in der Parameterliste als dritten Parameter ein.

    Im folgenden Codebeispiel wird gezeigt, wie die [**gettext \_**](swbemobjectex-gettext-.md) -Methode der-Instanz aufgerufen wird.

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  Optional können Sie überprüfen, ob es sich bei dem in Schritt 3 generierten XML-Code um wohl geformtes XML handelt, indem Sie ein XML-Dokumentobjektmodell (DOM)-Objekt erstellen und initialisieren und dann den XML-Text darin laden.

    Im folgenden Codebeispiel wird gezeigt, wie ein XML-DOM-Objekt erstellt und initialisiert und der XML-Text in dieses Objekt geladen wird.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Gibt die XML-Darstellung des-Objekts aus.

    Im folgenden Codebeispiel wird gezeigt, wie WScript verwendet wird, um den XML-Code auszugeben.

    ```VB
    wscript.echo strText
    ```

    

    Wenn Sie sich entschieden haben, das XML-DOM zu verwenden, um zu überprüfen, ob der generierte XML-Code wohl geformt ist, ersetzen Sie die vorherige Zeile durch Folgendes

    ```VB
    wscript.echo xml.xml
    ```

    

Das folgende VBScript-Codebeispiel enthält alle Schritte in der vorherigen Prozedur und codiert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse in XML, einschließlich der Klassen-, Eigenschaften-und Methoden Qualifizierer und ausgenommen der Systemeigenschaften.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

