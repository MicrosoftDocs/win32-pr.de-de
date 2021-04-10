---
description: Das Abrufen einer partiellen Instanz erfolgt, wenn WMI nur eine Teilmenge der Eigenschaften einer Instanz abruft.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Abrufen eines Teils einer WMI-Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d547ec2bbb7e3b53e22177cc0c48794dff22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215337"
---
# <a name="retrieving-part-of-a-wmi-instance"></a>Abrufen eines Teils einer WMI-Instanz

Das Abrufen einer partiellen Instanz erfolgt, wenn WMI nur eine Teilmenge der Eigenschaften einer Instanz abruft. WMI könnte z. b. nur die Eigenschaften **Name** und **Schlüssel** abrufen. Die häufigste Verwendung des Abrufs einer partiellen Instanz ist die Verwendung von großen Enumerationen mit mehreren Eigenschaften.

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a>Abrufen eines Teils einer WMI-Instanz mithilfe von PowerShell

Sie können eine einzelne Eigenschaft einer Instanz mithilfe von [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx); abrufen. die Eigenschaft selbst kann auf verschiedene Arten abgerufen und angezeigt werden. Wie beim Abrufen einer Instanz gibt PowerShell standardmäßig alle Instanzen einer bestimmten Klasse zurück. Sie müssen einen bestimmten Wert angeben, wenn Sie nur eine einzelne Instanz abrufen möchten.

Im folgenden Codebeispiel wird die Seriennummer des Volumes für eine Instanz der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse angezeigt.


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a>Abrufen eines Teils einer WMI-Instanz mit c# (System. Management)

Sie können eine einzelne Eigenschaft einer-Instanz abrufen, indem Sie ein neues [Management Object](/dotnet/api/system.management.managementobject) mithilfe der Details einer bestimmten-Instanz erstellen. Sie können dann implizit eine oder mehrere Eigenschaften der Instanz mit der [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) -Methode abrufen.

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

Im folgenden Codebeispiel wird die Seriennummer des Volumes für eine Instanz der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse angezeigt.


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a>Abrufen eines Teils einer WMI-Instanz mithilfe von VBScript

Sie können eine einzelne Eigenschaft einer Instanz mithilfe von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)abrufen.

Im folgenden Codebeispiel wird die Seriennummer des Volumes für eine Instanz der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse angezeigt.


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a>Abrufen eines Teils einer WMI-Instanz mithilfe von C++

Das folgende Verfahren wird verwendet, um einen Teil Instanzen Abruf mithilfe von C++ anzufordern.

**So fordern Sie einen Teil Instanzen Abruf mithilfe von C++ an**

1.  Erstellen Sie ein [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt mit einem Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Ein Kontext Objekt ist ein Objekt, das WMI verwendet, um weitere Informationen an einen WMI-Anbieter zu übergeben. In diesem Fall verwenden Sie das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt, um den Anbieter anzuweisen, einen Teil Instanzen Abruf zu verarbeiten.

2.  Fügen Sie \_ \_ get \_ Extensions, \_ \_ get \_ Ext \_ Client \_ Request und alle anderen benannten Werte hinzu, die die Eigenschaften beschreiben, die Sie an das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt abrufen möchten.

    In der folgenden Tabelle sind die unterschiedlichen benannten Werte aufgelistet, die im Abruf Befehl verwendet werden.

    

    | Benannter Wert                              | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_\_\_Erweiterungen erhalten<br/>           | **VT \_ Bool** auf **Variant \_ true** festgelegt. Wird verwendet, um zu signalisieren, dass Vorgänge zum Abrufen von Teil Instanzen verwendet werden. Dies ermöglicht eine schnelle, einmalige Überprüfung, ohne das gesamte Kontext Objekt aufzuzählen. Wenn einer der anderen Werte verwendet wird, muss dieser Wert lauten.<br/> |
    | \_\_\_Ext- \_ Eigenschaften erhalten<br/>      | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Zeichen folgen, die die abzurufenden Eigenschaften auflisten. Kann nicht gleichzeitig mit \_ \_ Get ext-Schlüsseln angegeben werden \_ \_ \_ .<br/> Ein Sternchen " \* " ist ein ungültiger Eigenschaftsname für \_ \_ get \_ Ext- \_ Eigenschaften.<br/>                    |
    | \_\_\_nur ext- \_ Schlüssel \_ erhalten<br/>      | **VT \_ Bool** auf **Variant \_ true** festgelegt. Gibt an, dass nur Schlüssel im zurückgegebenen-Objekt bereitgestellt werden sollen. Kann nicht gleichzeitig mit \_ \_ get \_ ext-Eigenschaften angegeben werden \_ . Stattdessen hat Vorrang vor den Eigenschaften von " \_ \_ get \_ ext" \_ .<br/>                            |
    | \_\_\_Ext- \_ Client \_ Anforderung anfordern<br/> | **VT \_ Bool** auf **Variant \_ true** festgelegt. Gibt an, dass der Aufrufer der Wert ist, der den Wert in das Kontext Objekt geschrieben hat, und dass er nicht von einem anderen abhängigen Vorgang weitergegeben wurde.<br/>                                                                        |

    

     

3.  Übergeben *Sie das* [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Kontext Objekt an alle Aufrufe von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices:: | ateinstanceenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)oder [**IWbemServices::**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) "".

    Durch das Übergeben des [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekts wird der Anbieter angewiesen, partielle Instanzabruf zuzulassen. Bei einem vollständigen Instanzabruf würden Sie *pctX* auf einen **null** -Wert festlegen. Wenn der Anbieter das Abrufen einer partiellen Instanz nicht unterstützt, erhalten Sie eine Fehlermeldung.

Wenn der Anbieter den partiellen Instanzvorgang nicht einhalten kann, fährt der Anbieter entweder so fort, als ob Sie das Kontext Objekt nicht eingegeben haben, oder gibt andernfalls den **\_ \_ nicht unterstützten \_ WBEM E-Parameter** zurück.

Im folgenden Beispiel wird beschrieben, wie Sie einen vollständigen Instanzabruf von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)ausführen und dann einen Teil Instanzen Abruf der **Win32 \_ LogicalDisk. Caption** -Eigenschaft ausführen.


```C++
#include <stdio.h>
#define _WIN32_DCOM
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#include <iostream>
using namespace std;
#include <comdef.h>


void main(void)
{
    HRESULT hr;
    _bstr_t bstrNamespace;
    IWbemLocator *pWbemLocator = NULL;
    IWbemServices *pServices = NULL;
    IWbemClassObject *pDrive = NULL;
    

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                         RPC_C_AUTHN_LEVEL_CONNECT,
                         RPC_C_IMP_LEVEL_IMPERSONATE,
                         NULL, EOAC_NONE, 0);
 
    if (FAILED(hr))
    {
       CoUninitialize();
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       return;
    }

    hr = CoCreateInstance(CLSID_WbemLocator, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemLocator, 
                          (void**) &pWbemLocator);
    if( FAILED(hr) ) 
    {
        CoUninitialize();
        printf("failed CoCreateInstance\n");
        return;
    }
    
    bstrNamespace = L"root\\cimv2";
    hr = pWbemLocator->ConnectServer(bstrNamespace, 
              NULL, NULL, NULL, 0, NULL, NULL, &pServices);
    if( FAILED(hr) ) 
    {
        pWbemLocator->Release();
        CoUninitialize();
        printf("failed ConnectServer\n");
        return;
    }
    pWbemLocator->Release();
    printf("Successfully connected to namespace.\n");

    
    BSTR bstrPath = 
         SysAllocString(L"Win32_LogicalDisk.DeviceID=\"C:\"");
   // *******************************************************//
   // Perform a full-instance retrieval. 
   // *******************************************************//
    hr = pServices->GetObject(bstrPath,
                              0,0, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed GetObject\n");
        return;
    }    
    // Display the object
    BSTR  bstrDriveObj;
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    pDrive->Release();
    pDrive = NULL;

   // *****************************************************//
   // Perform a partial-instance retrieval. 
   // *****************************************************//
    
    IWbemContext  *pctxDrive; // Create context object
    hr = CoCreateInstance(CLSID_WbemContext, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemContext, 
                          (void**) &pctxDrive);
    if (FAILED(hr))
    {
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("create instance failed for context object.\n");
        return;
    }
    
    VARIANT  vExtensions;
    VARIANT  vClient;
    VARIANT  vPropertyList;
    VARIANT  vProperty;
    SAFEARRAY  *psaProperties;
    SAFEARRAYBOUND saBounds;
    LONG  lArrayIndex = 0;
    
    // Add named values to the context object. 
    VariantInit(&vExtensions);
    V_VT(&vExtensions) = VT_BOOL;
    V_BOOL(&vExtensions) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXTENSIONS"), 
        0, &vExtensions);
    VariantClear(&vExtensions);

    VariantInit(&vClient);
    V_VT(&vClient) = VT_BOOL;
    V_BOOL(&vClient) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_CLIENT_REQUEST"), 
       0, &vClient);
    VariantClear(&vClient);
    // Create an array of properties to return.
    saBounds.cElements = 1;
    saBounds.lLbound = 0;
    psaProperties = SafeArrayCreate(VT_BSTR, 1, &saBounds);

    // Add the Caption property to the array.
    VariantInit(&vProperty);
    V_VT(&vProperty) = VT_BSTR;
    V_BSTR(&vProperty) = _bstr_t(L"Caption");
    SafeArrayPutElement(psaProperties, &lArrayIndex, 
       V_BSTR(&vProperty));
    VariantClear(&vProperty);
    
    VariantInit(&vPropertyList);
    V_VT(&vPropertyList) = VT_ARRAY | VT_BSTR;
    V_ARRAY(&vPropertyList) = psaProperties;
    // Put the array in the named value __GET_EXT_PROPERTIES.
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_PROPERTIES"), 
        0, &vPropertyList);
    VariantClear(&vPropertyList);
    SafeArrayDestroy(psaProperties);

    // Pass the context object as the pCtx parameter of GetObject.
    hr = pServices->GetObject(bstrPath, 0, pctxDrive, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed property GetObject\n");
        return;
    }    
    // Display the object
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    SysFreeString(bstrPath);

    VARIANT vFileSystem;
    // Attempt to get a property that was not requested.
    // The following should return a NULL property if
    // the partial-instance retrieval succeeded.

    hr = pDrive->Get(_bstr_t(L"FileSystem"), 0,
                       &vFileSystem, NULL, NULL);

    if( FAILED(hr) )
    { 
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("failed get for file system\n");
        return;
    }    
 
    if (V_VT(&vFileSystem) == VT_NULL)
        printf("file system variable is null - expected\n");
    else
        printf("FileSystem = %S\n", V_BSTR(&vFileSystem));
    
    VariantClear(&vFileSystem);

    pDrive->Release();    
    pctxDrive->Release();
    pServices->Release();
    pServices = NULL;    // MUST be set to NULL
    CoUninitialize();
    return;  // -- program successfully completed
};
```



Bei der Ausführung werden im vorangehenden Codebeispiel die folgenden Informationen geschrieben. Die erste Objektbeschreibung ist vom Abruf der vollständigen Instanz. Die zweite Objektbeschreibung basiert auf dem Abrufen von Teil Instanzen. Der letzte Abschnitt zeigt, dass Sie einen **null** -Wert erhalten, wenn Sie eine Eigenschaft anfordern, die im ursprünglichen [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Befehl nicht angefordert wurde.

``` syntax
Successfully connected to namespace

instance of Win32_LogicalDisk
{
        Caption = "C:";
        Compressed = FALSE;
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        FileSystem = "NTFS";
        FreeSpace = "3085668352";
        MaximumComponentLength = 255;
        MediaType = 12;
        Name = "C:";
        Size = "4581445632";
        SupportsFileBasedCompression = TRUE;
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "TITUS";
        VolumeName = "titus-c";
        VolumeSerialNumber = "7CB4B90E";
};

instance of Win32_LogicalDisk
{
        Caption = "C:";
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        MediaType = 12;
        Name = "C:";
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "MySystem";
};
```

Im vorherigen Beispiel wird die folgende Ausgabe generiert.

``` syntax
file system variable is null - expected
Press any key to continue
```

 

