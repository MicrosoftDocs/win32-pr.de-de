---
title: ResourceLocator. resourceUri-Eigenschaft (WSManDisp. h)
description: Ruft den Ressourcen-URI in einem ResourceLocator-Objekt ab oder legt ihn fest.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceUri-Eigenschaft Windows-Remoteverwaltung
- ResourceUri-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, resourceUri-Eigenschaft
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
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477688"
---
# <a name="resourcelocatorresourceuri-property"></a>ResourceLocator. resourceUri (Eigenschaft)

Ruft den Ressourcen- [*URI*](windows-remote-management-glossary.md) in einem [**ResourceLocator**](resourcelocator.md) -Objekt ab oder legt ihn fest. Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die Ressource identifiziert. Wenn Sie den Ressourcen-URI für ein [**ResourceLocator**](resourcelocator.md) -Objekt festlegen, darf der URI nur den Pfad enthalten.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie ein Beispiel für einen richtigen Pfad für [**resourceUri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

Der folgende Pfad funktioniert nicht, da er einen Schlüssel für eine bestimmte-Instanz enthält. Verwenden Sie die [**ResourceLocator. addselector**](resourcelocator-addselector.md) -Methode, um eine bestimmte Instanz anzugeben.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**Iwsmanresourcelocator:: resourceUri** ist die entsprechende C++-Methode.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





