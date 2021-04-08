---
title: Systemmonitor. Font (Eigenschaft)
description: Ruft die im-Steuerelement verwendete Schriftart ab oder legt Sie fest.
ms.assetid: 973ac31e-33e6-4280-ba0b-5b9f5f7563e7
keywords:
- Schriftart Eigenschaft (Sysmon)
- Font-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", Schriftart (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.Font
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2abf021000d673474bb006d9d16afa459ddbdb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741633"
---
# <a name="systemmonitorfont-property"></a>Systemmonitor. Font (Eigenschaft)

Ruft die im-Steuerelement verwendete Schriftart ab oder legt Sie fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property Font As stdole.IFontDisp
```



## <a name="property-value"></a>Eigenschaftswert

Schriftart, die zum Anzeigen von Text im-Steuerelement verwendet wird.

## <a name="remarks"></a>Bemerkungen

Dies ist eine Ambient-Eigenschaft. Der Wert dieser Eigenschaft wird vom Container bestimmt. Das Festlegen des Werts dieser Eigenschaft kann sich auf die Illusion des Steuer Elements und Containers auswirken, die eine einzelne Anwendung sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> <dt>

[**Systemmonitor. ForeColor**](systemmonitor-forecolor.md)
</dt> </dl>

 

 





