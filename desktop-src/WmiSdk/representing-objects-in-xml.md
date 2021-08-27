---
description: Generiert XML-Darstellungen von -Objekten.
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Darstellen von Objekten in XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae7eefc495cee7e515d699faf5074d187c726365d4723d9bbf443d346edb1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050378"
---
# <a name="representing-objects-in-xml"></a>Darstellen von Objekten in XML

Die XML-Encoderkomponente in WMI generiert XML-Darstellungen von -Objekten.

In C++ können Sie den XML-Encoder mit einem Aufruf der [**IWbemObjectTextSrc.GetText-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) starten, wobei Sie das in XML darzustellende Objekt und das Textformat angeben, das in der Darstellung verwendet werden soll. Weitere Informationen und ein Codebeispiel finden Sie unter So codieren Sie ein Objekt in XML mit C/C++.

Rufen Sie in VBScript oder Visual Basic zum Codieren von Daten für eine XML-Instanz [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md)auf. Weitere Informationen und ein Codebeispiel finden Sie unter So codieren Sie ein Objekt in XML mithilfe von VBScript.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Codieren eines Objekts mit C oder C++](#encode-an-object-using-c-or-c)
-   [Codieren eines Objekts mit VBScript](#encode-an-object-using-vbscript)
-   [Zugehörige Themen](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Codieren eines Objekts mit C oder C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

Im folgenden Verfahren wird beschrieben, wie ein Objekt in XML mit C oder C++ codiert wird.

**So codieren Sie ein Objekt in XML mit C oder C++**

1.  Richten Sie Ihr Programm für den Zugriff auf WMI-Daten ein.

    Da WMI auf COM-Technologie basiert, müssen Sie die erforderlichen Aufrufe der Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ausführen, um auf WMI zuzugreifen. Weitere Informationen finden Sie unter [Initialisieren von COM für eine WMI-Anwendung.](initializing-com-for-a-wmi-application.md)

2.  Erstellen Sie optional ein [**IWbemContext-Objekt,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) und initialisieren Sie es.

    Sie müssen das [**IWbemContext-Objekt**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) nur erstellen, wenn Sie den Standardvorgang ändern müssen. Das Kontextobjekt wird vom XML-Encoder verwendet, um die Menge an Informationen zu steuern, die in der XML-Darstellung des Objekts enthalten sind.

    In der folgenden Tabelle sind die optionalen Werte aufgeführt, die für das Kontextobjekt angegeben werden können.

    

    <table>
    <thead>
    <tr class="header">
    <th>Wert/Typ</th>
    <th>Bedeutung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;&quot; <strong>LocalOnly-VT_BOOL</strong></td>
    <td>True <strong></strong>gibt an, dass nur lokal in der Klasse definierte Eigenschaften und Methoden im resultierenden XML vorhanden sind. Der Standardwert ist <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;IncludeQualifiers &quot; <strong>VT_BOOL</strong></td>
    <td>Bei <strong>TRUE</strong>werden Klassen-, Instanz-, Eigenschaften- und Methodenqualifizierer in das resultierende XML eingeschlossen. Der Standardwert ist <strong>FALSE</strong>.</td>
    </tr>
    <tr class="odd">
    <td>&quot;ExcludeSystemProperties &quot; <strong>VT_BOOL</strong></td>
    <td>Bei <strong>TRUE</strong>werden WMI-Systemeigenschaften aus der Ausgabe herausgefiltert. Der Standardwert ist <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;&quot; <strong>PathLevel-VT_I4</strong></td>
    <td><dl> 0 = Ein <CLASS> - oder <INSTANCE> -Element wird generiert.<br />
1 = Ein <VALUE.NAMEDOBJECT> Element wird generiert.<br />
2 = Ein <VALUE.OBJECTWITHLOCALPATH> Element wird generiert.<br />
3 = A <VALUE.OBJECTWITHPATH> wird generiert.<br />
    </dl> Der Standardwert ist 0 (null).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    Das folgende Codebeispiel zeigt, wie das Kontextobjekt initialisiert wird, um Qualifizierer einzuschließen und Systemeigenschaften auszuschließen.

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

    

3.  Abrufen eines Verweises auf die Klasse oder Instanz, die in XML codiert werden soll.

    Nachdem Sie COM initialisiert haben und mit WMI verbunden sind, rufen [**Sie GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) auf, um einen Verweis auf die angegebene Klasse oder Instanz abzurufen. Wenn Sie einen BSTR zum Angeben der Klasse oder Instanz verwendet haben, rufen Sie [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) auf, um den von [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)belegten Arbeitsspeicher freizugeben.

    Im folgenden Codebeispiel wird ein Verweis auf eine [**Win32 \_ LogicalDisk-Instanz**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) abgerufen.

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

    

4.  Erstellen Sie ein [**IWbemObjectTextSrc-Objekt.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)

    Nachdem Sie über einen Verweis auf ein -Objekt verfügen, müssen Sie das [**IWbemObjectTextSrc-Objekt**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) mit einem Aufruf von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellen. Das **IWbemObjectTextSrc-Objekt** wird verwendet, um den tatsächlichen XML-Text zu generieren.

    Das folgende Codebeispiel zeigt, wie sie ein [**IWbemObjectTextSrc-Objekt**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) erstellen, indem [**Sie CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen.

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

    

5.  Rufen Sie die [**IWbemObjectTextSrc.GetText-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) auf, um eine XML-Darstellung eines Objekts abzurufen.

    Nachdem Sie den Kontext für die Darstellung des Objekts festgelegt, einen Verweis auf das Objekt erhalten und ein [**IWbemObjectTextSrc-Objekt**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) erstellt haben, können Sie eine XML-Darstellung des angegebenen Objekts generieren, indem Sie die [**IWbemObjectTextSrc.GetText-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) aufrufen.

    Der folgende C++-Beispielcode generiert eine XML-Darstellung des Objekts, auf das von *pClass* verwiesen wird. Die XML-Darstellung wird in *strText* zurückgegeben. Der dritte Parameter von [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) gibt das Für XML zu verwendende Textformat an und muss entweder WMI \_ OBJ \_ TEXT CIM \_ \_ DTD \_ 2 \_ 0 (0x1) oder WMI \_ OBJ TEXT \_ \_ WMI \_ DTD \_ 2 \_ 0 (0x2) sein. Weitere Informationen zu diesen Werten finden Sie unter [**IWbemObjectTextSrc::GetText-Parameterwerte.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext)

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

    

Der folgende C++-Beispielcode enthält alle Schritte in der vorherigen Prozedur und codiert die [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, einschließlich Klassen-, Eigenschafts- und Methodenqualifizierern und ohne Systemeigenschaften.


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

Im folgenden Verfahren wird beschrieben, wie ein Objekt in XML mithilfe von VBScript codiert wird.

**So codieren Sie ein Objekt in XML mit VBScript**

1.  Erstellen Sie optional ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) und initialisieren Sie es so, dass die für die XML-Darstellung erforderlichen Kontextwerte festgelegt werden.

    Das folgende Codebeispiel zeigt, wie die Werte den XML-Encoder anweisen, einen <VALUE zu generieren. OBJECTWITHLOCALPATH> -Element, einschließlich aller Qualifizierer und Ausschließen von Systemeigenschaften beim Erstellen der XML-Darstellung des Objekts.

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  Rufen Sie eine Instanz des Objekts oder der Klasse ab, das bzw. die in XML dargestellt werden soll.

    Im folgenden Codebeispiel wird eine Instanz des -Objekts abgerufen.

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Rufen [**Sie \_ die GetText-Methode**](swbemobjectex-gettext-.md) der im vorherigen Schritt erstellten Instanz auf. Verwenden Sie dabei 1 als Parameter, um das Textformat anzugeben, das CIM DTD Version 2.0 entspricht, oder 2, um das Textformat anzugeben, das WMI DTD Version 2.0 entspricht. Wenn Sie das [**SWbemNamedValueSet-Objekt**](swbemnamedvalueset.md) in Schritt 1 erstellt haben, fügen Sie es als dritten Parameter in die Parameterliste ein.

    Das folgende Codebeispiel zeigt, wie die [**GetText-Methode \_**](swbemobjectex-gettext-.md) der -Instanz aufgerufen wird.

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  Überprüfen Sie optional, ob es sich bei dem in Schritt 3 generierten XML-Code um wohlgeformte XML-Daten handelt, indem Sie ein XML-Dokumentobjektmodell -Objekt (DOM) erstellen und initialisieren und dann den XML-Text in dieses laden.

    Das folgende Codebeispiel zeigt, wie Sie ein XML-DOM-Objekt erstellen und initialisieren und den XML-Text darin laden.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Gibt die XML-Darstellung des Objekts aus.

    Im folgenden Codebeispiel wird veranschaulicht, wie wscript zum Ausgeben des XML-Codes verwendet wird.

    ```VB
    wscript.echo strText
    ```

    

    Wenn Sie sich für die Verwendung des XML-DOM entschieden haben, um zu überprüfen, ob der generierte XML-Code wohlgeformt ist, ersetzen Sie die vorherige Zeile durch Folgendes.

    ```VB
    wscript.echo xml.xml
    ```

    

Das folgende VBScript-Codebeispiel enthält alle Schritte in der vorherigen Prozedur und codiert die [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, einschließlich Klassen-, Eigenschafts- und Methodenqualifizierern und ohne Systemeigenschaften.


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

 

