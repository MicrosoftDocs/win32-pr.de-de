---
description: Ruft den Klassennamen und andere Informationen ab, die einer angegebenen GUID im Manifest einer Komponente zugeordnet sind.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Sxslookupclrguid-Funktion
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
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351246"
---
# <a name="sxslookupclrguid-function"></a>Sxslookupclrguid-Funktion

Ruft den Klassennamen und andere Informationen ab, die einer angegebenen GUID im Manifest einer Komponente zugeordnet sind. Diese Funktion wird nur verwendet, wenn die verwaltete, nicht verwaltete Interoperabilität auf niedriger Ebene in der .NET Framework implementiert wird. Weitere Informationen zur verwalteten, nicht verwalteten Interoperabilität finden Sie unter "Interoperabilität mit nicht verwaltetem Code" im .NET Framework SDK und auch in [isolierten Anwendungen und](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)parallelen Assemblys.

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

*dwFlags* \[ in\]
</dt> <dd>

Eine Kombination aus null oder mehr der folgenden Flags.



| Wert                                                                                                                                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SxS \_ Die \_ CLR- \_ GUID für die Suche \_ verwendet \_ ActCtx**</dt> <dt>0x00000001</dt> . </dl>              | Wenn dieses Flag festgelegt ist, muss der Parameter " *hactctx* " ein Aktivierungs Kontext Handle enthalten, das von der Funktion " [**deateactctx**](/windows/win32/api/winbase/nf-winbase-createactctxa) " zurückgegeben wird. Wenn dieses Flag nicht festgelegt ist, wird der Parameter " *hactctx* " ignoriert, und " **sxslookupclrguid** " durchsucht den derzeit aktiven Aktivierungs Kontext (die [**activateactctx**](/windows/win32/api/winbase/nf-winbase-activateactctx) -Funktion wird verwendet, um einen Aktivierungs Kontext aktiv zu machen).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SxS \_ Nachschlagen der \_ CLR- \_ GUID \_ Find \_ Ersatz**</dt> <dt>0x00010000 bis</dt> </dl>  | Wenn dieses Flag festgelegt ist, sucht **sxslookupclrguid** nach einem Ersatz Zeichen.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SxS \_ \_CLR- \_ GUID \_ Suchen \_ CLR- \_ Klasse**</dt> <dt>0x00020000</dt> </dl> | Wenn dieses Flag festgelegt ist, sucht **sxslookupclrguid** nach einer Klasse.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SxS \_ Nachschlagen der \_ CLR- \_ GUID \_ finden Sie \_ beliebige**</dt> <dt>0x00030000</dt> </dl>                    | Dabei handelt es sich um eine Kombination der **SxS-Lookup-CLR- \_ \_ \_ GUID \_ Find \_ Ersatz** und **SxS \_ Lookup \_ CLR \_ GUID \_ finden Sie \_ CLR- \_ klassenflags** . wenn beide festgelegt sind, sucht **sxslookupclrguid** zuerst nach einem Ersatz Zeichen und nur dann, wenn Sie eine Klasse finden.<br/>                                                                                                                                                |



 

</dd> <dt>

*pclsid* \[ in\]
</dt> <dd>

Ein Zeiger auf die GUID, über die im Aktivierungs Kontext nach Interoperation-Informationen gesucht werden soll. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*hactctx* \[ in, optional\]
</dt> <dd>

Wenn die **SxS-Lookup-CLR- \_ \_ \_ GUID das \_ \_ ActCtx** -Flag verwenden im *dwFlags* -Parameter festgelegt ist, muss " *hactctx* " ein Aktivierungs Kontext Handle enthalten, das von der Funktion " [**deateactctx**](/windows/win32/api/winbase/nf-winbase-createactctxa) " zurückgegeben wird. Andernfalls wird " *hactctx* " ignoriert.

</dd> <dt>

*pvoutputbuffer* \[ in, out, optional\]
</dt> <dd>

Zeiger auf den Puffer, in den Rückgabe Informationen kopiert werden. Dieser Parameter kann nur dann NULL-Wert sein, wenn der *cboutputbuffer* -Parameter den Wert NULL hat. Die Daten, die in diesem Puffer beim Beenden platziert werden (falls vorhanden), bestehen aus einer **SxS- \_ GUID- \_ Informations \_** Struktur, gefolgt von zusätzlichen Zeichen folgen Daten, die erforderlich sind. Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.

</dd> <dt>

*cboutputbuffer* \[ in\]
</dt> <dd>

Größe des Puffers in Byte, auf den durch den *pvoutputbuffer* -Parameter verwiesen wird.

</dd> <dt>

*pcboutputbuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, bei der die Größe (in Bytes) der Rückgabe Informationen beim Beenden platziert wird. Wenn der *cboutputbuffer* -Parameter 0 (null) ist, oder wenn die Größe des Ausgabepuffers kleiner ist als die Größe der Rückgabe Informationen, schlägt **sxslookupclrguid** fehl, und [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen Fehler aufgrund eines **\_ nicht ausreichenden \_ Puffers** zurück. Verwenden Sie in diesem Fall den Wert in der Variablen, auf die von *pcboutputbuffer* verwiesen wird, um einen ausreichend großen Puffer zuzuordnen, und rufen Sie dann erneut **sxslookupclrguid** auf, um die gewünschten Informationen abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . Weitere Fehlerinformationen erhalten Sie, wenn Sie [ **GetLastError** aufrufen.](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

Verwaltete Komponenten können sich selbst als Unterstützung verwalteter "Interop-Assemblys" deklarieren, damit ein nicht verwalteter Win32-Komponentenconsumer auf die deklarierende Assembly verweisen kann. Der Komponenten Consumer kann mit der verwalteten Komponente interagieren, indem [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für eine GUID aufgerufen wird. Die Interoperation-Ebene leitet die Objekt Erstellungs Anforderung an .NET Framework weiter, erstellt eine Instanz des verwalteten Objekts und gibt einen Schnittstellen Zeiger zurück.

**Sxslookupclrguid** ermöglicht den Frameworks das Abrufen von Informationen, die einer bestimmten GUID im Manifest der Komponente zugeordnet sind, z. b. den Namen der .NET-Klasse, die erforderliche Version der .NET Framework und die Hostassembly, in der Sie sich befindet. Verwaltete Komponenten veröffentlichen eine Interop-Assembly, die eine Reihe von Anweisungen enthält, die GUIDs mit Assemblynamen und Typnamen verknüpfen, und die .NET-Runtime brottet die Konstruktion verwalteter Objektinstanzen, wenn [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen wird.

Im folgenden finden Sie ein Beispiel für ein Komponenten Manifest, das eine CLR-GUID und ein CLR-Ersatz Zeichen deklariert, das **sxslookupclrguid** suchen kann:

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

Ein Interoperation-Anbieter ruft **sxslookupclrguid** mit einem Zeiger auf die GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" auf. und erhalten in Rückgabe den Klassennamen "mysampleersatz", die erforderliche Laufzeitversion "1.0.3055" und die Text Identität "dotnet. Sample. Surrogates, Version = ' 1.0.0.0 ', Type = ' Interop '" der Hostingkomponente.

Diese Rückgabe Informationen sind enthalten und/oder referenziert durch eine **SxS- \_ GUID- \_ Informations- \_ CLR** -Struktur, die wie folgt deklariert wird.

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

Die Elemente dieser Struktur enthalten die folgenden Informationen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Member</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>CBSIZE</strong><br/></td>
<td>Enthält die Größe der SXS_GUID_INFORMATION_CLR Struktur (Dadurch kann die-Struktur in späteren Versionen vergrößert werden).<br/></td>
</tr>
<tr class="even">
<td><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong><br/></td>
<td>Enthält einen der folgenden zwei Flagwerte: <br/>
<ul>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): gibt an, dass die angegebene GUID einem Ersatz Zeichen zugeordnet wurde &quot; .&quot;</li>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): gibt an, dass die angegebene GUID einer Klasse zugeordnet wurde &quot; .&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszruntimeversion</strong><br/></td>
<td>Verweist auf eine NULL terminierte breit Zeichen-Zeichenfolge, die die Version der Laufzeit identifiziert, die im Host Manifest für diese Klasse angegeben ist.<br/></td>
</tr>
<tr class="even">
<td><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwsztypame</strong><br/></td>
<td>Verweist auf eine NULL terminierte breit Zeichen-Zeichenfolge, die den Namen der .NET-Klasse enthält, die der angegebenen GUID zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszassemblyidentity</strong><br/></td>
<td>Verweist auf eine NULL terminierte breit Zeichen-Zeichenfolge, die die Text Identität der Assembly enthält, die diese Klasse hostet. Weitere Informationen zur Text Identität finden Sie &quot; unter Angeben von voll qualifizierten Typnamen unter "ermitteln &quot; &quot; von Typinformationen zur Laufzeit" &quot; unter &quot; Programmieren mit der .NET Framework &quot; im .NET Framework SDK.<br/></td>
</tr>
</tbody>
</table>



 

Eine nicht verwaltete Anwendung kann die auf diese Weise zurückgegebenen Informationen verwenden, um die richtige Version des .NET Framework zu laden, die Assembly zu laden, die durch das **pcwszassemblyidentity** -Element identifiziert wird, und dann eine Instanz der Klasse zu erstellen, die durch das **pcwsztywatame** -Element benannt wird.

## <a name="examples"></a>Beispiele

Verwenden Sie das dynamische verknüpfen wie folgt, um die **sxslookupclrguid** -Funktion aufzurufen:


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Isolierte Anwendungen und parallele Assemblys](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**"Kreateactctx"**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**Activateactctx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
