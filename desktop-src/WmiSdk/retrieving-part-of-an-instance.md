---
description: Ein Teilweiser Instanzabruf ist , wenn WMI nur eine Teilmenge der Eigenschaften einer Instanz abruft.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Abrufen eines Teils einer WMI-Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cce9d809e5203b7c00f2b2297403f835d98f37ff86641e297673ee50e579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316214"
---
# <a name="retrieving-part-of-a-wmi-instance"></a>Abrufen eines Teils einer WMI-Instanz

Ein Teilweiser Instanzabruf ist , wenn WMI nur eine Teilmenge der Eigenschaften einer Instanz abruft. WMI kann z. B. nur die **Eigenschaften Name** und **Schlüssel** abrufen. Die häufigste Verwendung des teilweisen Instanzabrufs ist bei großen Enumerationen mit mehreren Eigenschaften.

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a>Abrufen eines Teils einer WMI-Instanz mithilfe von PowerShell

Sie können eine einzelne Eigenschaft einer Instanz abrufen, indem Sie [Get-WmiObject verwenden.](https://technet.microsoft.com/library/dd315379.aspx) Die Eigenschaft selbst kann auf verschiedene Weise abgerufen und angezeigt werden. Wie beim Abrufen einer Instanz gibt PowerShell standardmäßig alle Instanzen einer bestimmten Klasse zurück. Sie müssen einen bestimmten Wert angeben, wenn Sie nur eine einzelne Instanz abrufen möchten.

Im folgenden Codebeispiel wird die Seriennummer des Volumes für eine Instanz der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) angezeigt.


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a>Abrufen eines Teils einer WMI-Instanz mithilfe von C# (System.Management)

Sie können eine einzelne Eigenschaft einer Instanz abrufen, indem Sie ein neues [ManagementObject mithilfe](/dotnet/api/system.management.managementobject) der Details einer bestimmten Instanz erstellen. Sie können dann implizit eine oder mehrere Eigenschaften der -Instanz mit der [GetPropertyValue-Methode](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) abrufen.

> [!Note]  
> **System.Management war** der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. Die APIs in diesem Namespace sind jedoch im Allgemeinen langsamer und werden im Vergleich zu ihren moderneren **Microsoft.Management.Infrastructure-Entsprechungen** nicht so gut skaliert.

 

Im folgenden Codebeispiel wird die Seriennummer des Volumes für eine Instanz der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) angezeigt.


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a>Abrufen eines Teils einer WMI-Instanz mit VBScript

Sie können eine einzelne Eigenschaft einer Instanz abrufen, indem Sie [**GetObject verwenden.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)

Im folgenden Codebeispiel wird die Seriennummer des Volumes für eine Instanz der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) angezeigt.


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a>Abrufen eines Teils einer WMI-Instanz mit C++

Das folgende Verfahren wird verwendet, um einen teilweisen Instanzabruf mithilfe von C++ an fordern.

**So fordern Sie einen Teilabruf einer Instanz mit C++ an**

1.  Erstellen Sie [**ein IWbemContext-Objekt**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) mit einem Aufruf von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Ein Kontextobjekt ist ein Objekt, das WMI verwendet, um weitere Informationen an einen WMI-Anbieter zu übergeben. In diesem Fall verwenden Sie das [**IWbemContext-Objekt,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) um den Anbieter anweisen, einen abrufweisen Teil der Instanz zu verarbeiten.

2.  Fügen Sie GET EXTENSIONS, GET EXT CLIENT REQUEST und alle anderen benannten Werte hinzu, die die Eigenschaften beschreiben, die Sie für das \_ \_ \_ \_ \_ \_ \_ \_ [**IWbemContext-Objekt abrufen**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) möchten.

    In der folgenden Tabelle sind die verschiedenen benannten Werte aufgeführt, die in Ihrem Abrufaufruf verwendet werden.

    

    | Benannter Wert                              | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_\_ERWEITERUNGEN \_ ERHALTEN<br/>           | **VT \_ BOOL auf** **VARIANT TRUE \_ festgelegt.** Wird verwendet, um zu signalisieren, dass Abrufvorgänge für partielle Instanzen verwendet werden. Dies ermöglicht eine schnelle, einzelne Überprüfung, ohne das gesamte Kontextobjekt aufzählen zu müssen. Wenn einer der anderen Werte verwendet wird, muss dieser sein.<br/> |
    | \_\_GET \_ EXT PROPERTIES (EXT-EIGENSCHAFTEN \_ ERHALTEN)<br/>      | [**SAFEARRAY von**](/windows/win32/api/oaidl/ns-oaidl-safearray) Zeichenfolgen, die die abzurufenden Eigenschaften auflisten. Kann nicht gleichzeitig mit \_ \_ GET EXT KEYS ONLY \_ angegeben \_ \_ werden.<br/> Ein Sternchen " \* " ist ein ungültiger Eigenschaftenname für \_ \_ GET EXT \_ \_ PROPERTIES.<br/>                    |
    | \_\_NUR \_ \_ EXT-SCHLÜSSEL \_ ERHALTEN<br/>      | **VT \_ BOOL auf** **VARIANT TRUE \_ festgelegt.** Gibt an, dass nur Schlüssel im zurückgegebenen -Objekt bereitgestellt werden sollen. Kann nicht gleichzeitig mit \_ \_ GET EXT PROPERTIES \_ angegeben \_ werden. Stattdessen hat Vorrang vor \_ \_ GET EXT \_ \_ PROPERTIES.<br/>                            |
    | \_\_GET \_ EXT \_ CLIENT \_ REQUEST<br/> | **VT \_ BOOL auf** **VARIANT TRUE \_ festgelegt.** Gibt an, dass der Aufrufer der Aufrufer war, der den Wert in das Kontextobjekt geschrieben hat und nicht von einem anderen abhängigen Vorgang übertragen wurde.<br/>                                                                        |

    

     

3.  Übergeben Sie das [**IWbemContext-Kontextobjekt**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) über den *pCtx-Parameter* an alle Aufrufe von [**IWbemServices::GetObject,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) [**IWbemServices::GetObjectAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)oder [**IWbemServices::CreateInstanceEnumAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)

    Durch Übergeben [**des IWbemContext-Objekts**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) wird der Anbieter angewiesen, teilweise Instanzabrufe zu ermöglichen. Bei einem vollständigen Instanzabruf würden Sie *pCtx* auf einen **NULL-Wert** festlegen. Wenn der Anbieter den Abruf von Teilinstanzen nicht unterstützt, erhalten Sie eine Fehlermeldung.

Wenn der Anbieter dem Teilinstanzvorgang nicht entsprechen kann, geht der Anbieter entweder so vor, als ob Sie das Kontextobjekt nicht eingeben würden, oder gibt **WBEM \_ E \_ UNSUPPORTED \_ PARAMETER zurück.**

Im folgenden Beispiel wird beschrieben, wie sie einen vollständigen Instanzabruf von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)ausführen und dann einen teilinstanzenbasierten Abruf der **Win32 \_ LogicalDisk.Caption-Eigenschaft** ausführen.


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



Bei der Ausführung schreibt das vorherige Codebeispiel die folgenden Informationen. Die erste Objektbeschreibung wird aus dem vollständigen Instanzabruf erstellt. Die zweite Objektbeschreibung wird aus dem Abruf der partiellen Instanz erstellt. Der letzte Abschnitt zeigt, dass Sie einen **NULL-Wert** erhalten, wenn Sie eine Eigenschaft anfordern, die im ursprünglichen [**GetObject-Aufruf nicht angefordert**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) wurde.

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

Die folgende Ausgabe wird im vorherigen Beispiel generiert.

``` syntax
file system variable is null - expected
Press any key to continue
```

 

