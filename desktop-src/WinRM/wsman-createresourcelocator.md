---
title: WSMan.CreateResourceLocator-Methode (WSManDisp.h)
description: Erstellt ein ResourceLocator-Objekt, das verwendet werden kann, anstatt einen Ressourcen-URI in Sitzungsobjektvorgängen wie Session.Get, Session.Put oder Session.Enumerate anzugeben.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- CreateResourceLocator-Methode Windows Remoteverwaltung
- CreateResourceLocator-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung, CreateResourceLocator-Methode
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
ms.openlocfilehash: 2d78276f40ee6e2e1aff10f17bc9f41bb1d1e4aa32cde68a41842c5cee8b95bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742612"
---
# <a name="wsmancreateresourcelocator-method"></a>WSMan.CreateResourceLocator-Methode

Erstellt ein [**ResourceLocator-Objekt,**](resourcelocator.md) das verwendet werden kann, anstatt einen Ressourcen-URI in [**Sitzungsobjektvorgängen**](session.md) wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)anzugeben.

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

Der Ressourcen-URI für die Ressource. Weitere Informationen zu URI-Zeichenfolgen finden Sie unter [Ressourcen-URIs.](resource-uris.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**ResourceLocator-Objekt,**](resourcelocator.md) das dann zum Ausführen lokaler oder Remote-WinRM-Vorgänge verwendet werden kann.

## <a name="remarks"></a>Hinweise

Wenn die **FragmentDialect-Eigenschaft** nicht im [**ResourceLocator-Objekt**](resourcelocator.md) angegeben ist, ist der Standardwert die XPath 1.0-Spezifikation. Weitere Informationen finden Sie unter [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein [**ResourceLocator-Objekt**](resourcelocator.md) erstellt und der Wert der **Description-Eigenschaft** des Netzwerkadapters aus der Instanz von [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) mit dem Index "1" ermittelt.


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> </dl>

 

