---
title: LVM_GETGROUPINFOBYINDEX Meldung (kommstrg. h)
description: Ruft Informationen zu einer angegebenen Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getgroupinfobyindex-Makros.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Windows-Steuerelemente für LVM_GETGROUPINFOBYINDEX Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104457"
---
# <a name="lvm_getgroupinfobyindex-message"></a>LVM \_ getgroupinfobyindex-Meldung

Ruft Informationen zu einer angegebenen Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getgroupinfobyindex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der Index der Gruppe.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**orgroup**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) -Struktur, die Informationen über die von *wParam* angegebene Gruppe empfangen soll. Der aufrufende Prozess ist für die Zuordnung von Arbeitsspeicher für die Struktur und alle Puffer in der Struktur verantwortlich, wie z. b. den, auf den das **pszheader** -Element zeigt. Legen Sie alle Kontingenten Elemente der Struktur fest, z. b. **cchheader** die Größe des Puffers, auf den **pszheader** in **WCHARs** zeigt, einschließlich des abschließenden **null**-Zeichens. Legen Sie **CBSIZE** auf sizeof (LVGROUP) fest.

Der Nachrichtenempfänger ist dafür verantwortlich, die Strukturmember mit Informationen für die von *wParam* angegebene Gruppe festzulegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





