---
title: ResourceLocator. addselector-Methode (WSManDisp. h)
description: Fügt dem ResourceLocator-Objekt einen Selektor hinzu. Der Selektor gibt eine bestimmte Instanz einer Ressource an.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Addselector-Methode Windows-Remoteverwaltung
- Addselector-Methode Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, addselector-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956516"
---
# <a name="resourcelocatoraddselector-method"></a>ResourceLocator. addselector-Methode

Fügt dem [**ResourceLocator**](resourcelocator.md) -Objekt einen [*Selektor*](windows-remote-management-glossary.md) hinzu. Der Selektor gibt eine bestimmte Instanz einer *Ressource* an. Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceselname* \[ in\]
</dt> <dd>

Der Name der Auswahl. Wenn z. b. WMI-Daten angefordert werden, handelt es sich bei diesem Parameter um die Schlüsseleigenschaft für eine WMI-Klasse.

</dd> <dt>

*selvalue* \[ in\]
</dt> <dd>

Der Auswahl Wert. Für WMI-Daten enthält dieser Parameter z. b. einen Wert für eine Schlüsseleigenschaft, die eine bestimmte Instanz identifiziert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Iwsmanresourcelocator:: addselector** ist die entsprechende C++-Methode.

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

 

 





