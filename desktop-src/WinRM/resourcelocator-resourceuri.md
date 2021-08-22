---
title: ResourceLocator.ResourceURI-Eigenschaft (WSManDisp.h)
description: Ruft den Ressourcen-URI in einem ResourceLocator-Objekt ab oder legt den Ressourcen-URI fest.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceURI-Eigenschaft Windows Remoteverwaltung
- ResourceURI-Eigenschaft Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung, ResourceURI-Eigenschaft
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323240462dad32ba757897798b663b78b373ebb3ab3e60c3387dd7da8eef4c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642860"
---
# <a name="resourcelocatorresourceuri-property"></a>ResourceLocator.ResourceURI-Eigenschaft

Ruft den [*Ressourcen-URI*](windows-remote-management-glossary.md) in einem [**ResourceLocator-Objekt**](resourcelocator.md) ab oder legt den Ressourcen-URI fest. Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) angeben, anstatt einen Ressourcen-URI in [**Sitzungsobjektvorgängen**](session.md) wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)anzugeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die Ressource identifiziert. Beim Festlegen des Ressourcen-URI für ein [**ResourceLocator-Objekt**](resourcelocator.md) darf der URI nur den Pfad enthalten.

## <a name="remarks"></a>Hinweise

Im Folgenden wird ein Beispiel für einen ordnungsgemäßen Pfad für [**ResourceURI beschrieben.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri)

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

Der folgende Pfad funktioniert nicht, da er einen Schlüssel für eine bestimmte Instanz enthält. Verwenden Sie die [**ResourceLocator.AddSelector-Methode,**](resourcelocator-addselector.md) um eine bestimmte Instanz anzugeben.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator::ResourceURI** ist die entsprechende C++-Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 





