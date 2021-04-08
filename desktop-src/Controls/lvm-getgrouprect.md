---
title: LVM_GETGROUPRECT Meldung (kommstrg. h)
description: Ruft das Rechteck für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getgrouprect-Makros.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- Windows-Steuerelemente für LVM_GETGROUPRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949463"
---
# <a name="lvm_getgrouprect-message"></a>LVM \_ getgrouprect-Nachricht

Ruft das Rechteck für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getgrouprect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Gibt die Group by **igroupid** an (siehe Struktur von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ").

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die Informationen über die von *wParam* angegebene Gruppe empfangen soll. Der Nachrichtenempfänger ist dafür verantwortlich, die Strukturmember mit Informationen für die von *wParam* angegebene Gruppe festzulegen.

Der Aufrufprozess ist für die Zuordnung von Arbeitsspeicher für die Struktur verantwortlich. Legen Sie den **obersten** Member des [**Rect**](/previous-versions//dd162897(v=vs.85)) auf eines der folgenden Flags fest, um die Koordinaten des Rechtecks anzugeben, das Sie erhalten möchten.



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**Gruppe "lvggr" \_**</dt> </dl>                | Koordinaten der gesamten erweiterten Gruppe.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**lvggr- \_ Header**</dt> </dl>             | Nur Koordinaten des Headers (reduzierte Gruppe).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**Bezeichnung "lvggr" \_**</dt> </dl>                | Nur Koordinaten der Bezeichnung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**subsetlink für "lvggr" \_**</dt> </dl> | Nur Koordinaten der Teilmenge (Markup Teilmenge). Ein Listenansicht-Steuerelement kann die Anzahl der sichtbaren Elemente einschränken, die in jeder Gruppe angezeigt werden. Dem Benutzer wird ein Link angezeigt, mit dem der Benutzer die Gruppe erweitern kann. Dieses Flag gibt das umgebende Rechteck der Teilmenge zurück, wenn es sich bei der Gruppe um eine Teilmenge handelt (Gruppenstatus der \_ untergeordneten Gruppen. [](/windows/win32/api/commctrl/ns-commctrl-lvgroup)  Dieses Flag wird bereitgestellt, damit Barrierefreiheits Anwendungen den Link finden können.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

