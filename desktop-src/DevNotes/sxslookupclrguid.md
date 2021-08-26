---
description: Ruft den Klassennamen und andere Informationen ab, die einer bestimmten GUID im Manifest einer Komponente zugeordnet sind.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 516ba97eb70defdbc6f92efa5c65e6d23246fe67
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465597"
---
# <a name="sxslookupclrguid-function"></a>SxsLookupClrGuid-Funktion

Ruft den Klassennamen und andere Informationen ab, die einer bestimmten GUID im Manifest einer Komponente zugeordnet sind. Diese Funktion wird nur verwendet, wenn verwaltete und nicht verwaltete Interoperabilität auf niedriger Ebene im .NET Framework implementiert wird. Weitere Informationen zur verwalteten und nicht verwalteten Interoperabilität finden Sie unter "Interoperating with Unmanaged Code" (Interoperabilität mit nicht verwaltetem Code) im .NET Framework SDK und [isolierte Anwendungen und parallele Assemblys.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

## <a name="syntax"></a>Syntax


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Eine Kombination aus 0 (null) oder mehr der folgenden Flags.



| Wert                                                                                                                                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR \_ GUID \_ USE \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Wenn dieses Flag festgelegt ist, muss der *hActCtx-Parameter* ein Aktivierungskontexthandle enthalten, das von der [**CreateActCtx-Funktion**](/windows/win32/api/winbase/nf-winbase-createactctxa) zurückgegeben wird. Wenn dieses Flag nicht festgelegt ist, wird der *hActCtx-Parameter* ignoriert, und **SxsLookupClrGuid** durchsucht den derzeit aktiven Aktivierungskontext (die [**ActivateActCtx-Funktion**](/windows/win32/api/winbase/nf-winbase-activateactctx) wird verwendet, um einen Aktivierungskontext zu aktivieren).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR \_ GUID \_ FIND \_ SURROGATE**</dt> <dt>0x00010000</dt> </dl>  | Wenn dieses Flag festgelegt ist, sucht **SxsLookupClrGuid** nach einem Ersatzzeichen.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR \_ GUID \_ FIND \_ CLR \_ CLASS**</dt> <dt>0x00020000</dt> </dl> | Wenn dieses Flag festgelegt ist, sucht **SxsLookupClrGuid** nach einer Klasse.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR \_ GUID \_ FIND \_ ANY**</dt> <dt>0x00030000</dt> </dl>                    | Dies ist eine Kombination aus den **FLAGs SXS \_ LOOKUP \_ CLR \_ GUID \_ FIND \_ SURROGATE** und **SXS \_ LOOKUP \_ CLR \_ GUID \_ FIND \_ CLR \_ CLASS.** Wenn beide festgelegt sind, sucht **SxsLookupClrGuid** zuerst nach einem Ersatzzeichen, und nur wenn es keins findet, sucht es nach einer Klasse.<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[ In\]
</dt> <dd>

Ein Zeiger auf die GUID, über die der Aktivierungskontext nach Interoperationsinformationen durchsucht werden soll. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*hActCtx* \[ in, optional\]
</dt> <dd>

Wenn das **SXS \_ LOOKUP \_ CLR \_ GUID \_ USE \_ ACTCTX-Flag** im *dwFlags-Parameter* festgelegt ist, muss *hActCtx* ein Aktivierungskontexthandle enthalten, das von der [**CreateActCtx-Funktion**](/windows/win32/api/winbase/nf-winbase-createactctxa) zurückgegeben wird. Andernfalls wird *hActCtx* ignoriert.

</dd> <dt>

*pvOutputBuffer* \[ in, out, optional\]
</dt> <dd>

Zeiger auf den Puffer, in den Rückgabeinformationen kopiert werden. Dieser Parameter kann nur nullwertig sein, wenn der *cbOutputBuffer-Parameter* nullwertig ist. Die Daten, die beim Beenden (falls vorhanden) in diesem Puffer platziert werden, bestehen aus einer **\_ SXS GUID \_ INFORMATION \_ CLR-Struktur,** gefolgt von allen erforderlichen zusätzlichen Zeichenfolgendaten. Weitere Informationen finden Sie weiter unten im Abschnitt "Hinweise".

</dd> <dt>

*cbOutputBuffer* \[ In\]
</dt> <dd>

Größe des Puffers, auf den der *pvOutputBuffer-Parameter* zeigt, in Bytes.

</dd> <dt>

*pwOutputBuffer* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, in der die Größe der Rückgabeinformationen beim Beenden in Bytes platziert wird. Wenn der *cbOutputBuffer-Parameter* 0 (null) ist oder die Größe des Ausgabepuffers kleiner als die Größe der Rückgabeinformationen ist, schlägt **SxsLookupClrGuid** fehl, und [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehler **ERROR INSUFFICIENT \_ \_ BUFFER** zurück. Verwenden Sie in diesem Fall den Wert in der Variablen, auf die von *"pwOutputBuffer"* verwiesen wird, um einen ausreichend großen Puffer zuzuordnen, und rufen Sie dann **erneut SxsLookupClrGuid** auf, um die gewünschten Informationen abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.** Weitere Fehlerinformationen erhalten Sie, wenn [ **Sie GetLastError** aufrufen.](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

Verwaltete Komponenten können sich selbst als unterstützend für verwaltete "Interopassemblys" deklarieren, damit ein nicht verwalteter Win32-Komponentenverbraucher auf die deklarierende Assembly verweisen kann. Der Komponentenverbraucher kann mit der verwalteten Komponente interagieren, indem [**er CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf einer GUID aufruft. Die Interoperationsebene leitet die Objekterstellungsanforderung an .NET Framework weiter, erstellt eine Instanz des verwalteten Objekts und gibt einen Schnittstellenzeiger zurück.

**SxsLookupClrGuid** ermöglicht den Frameworks das Abrufen von Informationen, die einer bestimmten GUID im Manifest der Komponente zugeordnet sind, z. B. den Namen der .NET-Klasse, die version der benötigten .NET Framework und die Hostassembly, in der sie sich befindet. Verwaltete Komponenten veröffentlichen eine Interopassembly, die eine Reihe von Anweisungen enthält, die GUIDs Assembly- und Typnamen zuordnen, und die .NET-Laufzeit vermittelt die Erstellung verwalteter Objektinstanzen, wenn [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen wird.

Im Folgenden finden Sie ein Beispielkomponentenmanifest, das eine CLR-GUID und ein CLR-Ersatzzeichen deklariert, nach dem **SxsLookupClrGuid** suchen kann:

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

Ein Interoperationsanbieter würde **SxsLookupClrGuid** mit einem Zeiger auf die GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" aufrufen. und erhalten als Rückgabe den Klassennamen "MySampleSurrogate", die erforderliche Runtimeversion "1.0.3055" und die Textidentität "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" der Hostingkomponente.

Diese Rückgabeinformationen werden in einer **SXS \_ GUID \_ INFORMATION \_ CLR-Struktur** enthalten und/oder referenziert, die wie folgt deklariert ist.

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

Die Member dieser Struktur enthalten die folgenden Informationen.




| Member | BESCHREIBUNG | 
|--------|-------------|
| <span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong><br /> | Enthält die Größe der SXS_GUID_INFORMATION_CLR -Struktur (dadurch kann die Struktur in späteren Versionen vergrößert werden).<br /> | 
| <span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>Dwflags</strong><br /> | Enthält einen der folgenden beiden Flagwerte: <br /><ul><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Gibt an, dass die angegebene GUID einem "Ersatzzeichen" zugeordnet wurde.</li><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Gibt an, dass die angegebene GUID einer "Klasse" zugeordnet wurde.</li></ul> | 
| <span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br /> | Zeigt auf eine auf null endende Breitzeichenzeichenfolge, die die Version der Laufzeit identifiziert, die im Hostmanifest für diese Klasse angegeben ist.<br /> | 
| <span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br /> | Zeigt auf eine auf null endende Breitzeichenzeichenfolge, die den Namen der .NET-Klasse enthält, die der angegebenen GUID zugeordnet ist.<br /> | 
| <span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br /> | Zeigt auf eine auf null endende Breitzeichenzeichenfolge, die die Textidentität der Assembly enthält, die diese Klasse hostet. Weitere Informationen zur Textidentität finden Sie unter "Angeben von vollqualifizierten Typnamen" unter "Ermitteln von Typinformationen zur Laufzeit" unter "Programmieren mit dem .NET Framework" im .NET Framework SDK.<br /> | 




 

Eine nicht verwaltete Anwendung kann die auf diese Weise zurückgegebenen Informationen verwenden, um die richtige Version des .NET Framework zu laden, die durch das **pcwszAssemblyIdentity-Element** identifizierte Assembly zu laden und dann eine Instanz der Klasse zu erstellen, die durch das **pcwszTypeName-Element** benannt wird.

## <a name="examples"></a>Beispiele

Verwenden Sie die dynamische Verknüpfung wie folgt, um die **SxsLookupClrGuid-Funktion** aufzurufen:


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Isolierte Anwendungen und parallele Assemblys](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
