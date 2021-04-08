---
title: WSMAN. kreateresourcelocator-Methode (WSManDisp. h)
description: Erstellt ein ResourceLocator-Objekt, das verwendet werden kann, anstatt einen Ressourcen-URI in Sitzungs Objekt Vorgängen wie "Session. Get", "Session. Put" oder "Session. Enumerate" anzugeben.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung der Methode "kreateresourcelocator"
- Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Methode "kreateresourcelocator"
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949791"
---
# <a name="wsmancreateresourcelocator-method"></a>WSMAN. kreateresourcelocator-Methode

Erstellt ein [**ResourceLocator**](resourcelocator.md) -Objekt, das verwendet werden kann, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.

## <a name="syntax"></a>Syntax


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URI* \[ in, optional\]
</dt> <dd>

Der Ressourcen-URI für die Ressource. Weitere Informationen zu URI-Zeichen folgen finden Sie unter [Ressourcen-URIs](resource-uris.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**ResourceLocator**](resourcelocator.md) -Objekt, das dann zum Ausführen von lokalen oder Remote-WinRM-Vorgängen verwendet werden kann.

## <a name="remarks"></a>Bemerkungen

Wenn die **Fragmentdialekt** -Eigenschaft im [**ResourceLocator**](resourcelocator.md) -Objekt nicht angegeben ist, ist der Standardwert die XPath 1,0-Spezifikation. Weitere Informationen finden Sie unter [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein [**ResourceLocator**](resourcelocator.md) -Objekt erstellt und der Eigenschafts Wert für die Netzwerkadapter **Beschreibung** aus der Instanz von [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) mit dem Index "1" abgerufen.


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WSMAN**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

