---
title: Vmundoaction-Enumeration (vpccominterfaces. h)
description: Gibt an, was mit rückgängig-Laufwerken geschieht, wenn ein virtueller Computer heruntergefahren oder ausgeschaltet wird.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Virtueller PC der vmundoaction-Enumeration
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518905"
---
# <a name="vmundoaction-enumeration"></a>Vmundoaction-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt an, was mit rückgängig-Laufwerken geschieht, wenn ein virtueller Computer heruntergefahren oder ausgeschaltet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmundoaction \_ verwerfen**
</dt> <dd>

Verwerfen der rückgängig-Laufwerke die übergeordneten Laufwerke bleiben unverändert.

</dd> <dt>

<span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmundoaction \_ beibehalten**
</dt> <dd>

Behalten Sie die rückgängig-Laufwerke. die übergeordneten Laufwerke bleiben unverändert, Änderungen werden jedoch beim nächsten Start des virtuellen Computers beibehalten.

</dd> <dt>

<span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmundoaction- \_ Commit**
</dt> <dd>

Commit für Änderungen an den übergeordneten Laufwerken.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine:: UndoAction**](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

