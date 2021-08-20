---
title: LVM_GETGROUPRECT (Commctrl.h)
description: Ruft das Rechteck für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ GetGroupRect-Makros.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT meldungssteuerelemente Windows
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
ms.openlocfilehash: 89340015972799b059e4568b5e87be511b7fc3718e7e7494d1bf46296886f030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540920"
---
# <a name="lvm_getgrouprect-message"></a>LVM \_ GETGROUPRECT-Nachricht

Ruft das Rechteck für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetGroupRect-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Gibt die Gruppe nach **iGroupId an** (siehe [**LVGROUP-Struktur).**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) um Informationen zu der durch *wParam* angegebenen Gruppe zu empfangen. Der Nachrichtenempfänger ist dafür verantwortlich, die Strukturmitglieder mit Informationen für die durch *wParam* angegebene Gruppe festzulegen.

Der aufrufende Prozess ist für die Zuweisung von Arbeitsspeicher für die -Struktur verantwortlich. Legen Sie **den obersten** Member des [**RECT**](/previous-versions//dd162897(v=vs.85)) auf eines der folgenden Flags fest, um die Koordinaten des zu erhaltenden Rechtecks anzugeben.



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**\_LVGGR-GRUPPE**</dt> </dl>                | Koordinaten der gesamten erweiterten Gruppe.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**LVGGR-HEADER \_**</dt> </dl>             | Nur Koordinaten des Headers (reduzierte Gruppe).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**LVGGR-BEZEICHNUNG \_**</dt> </dl>                | Nur Koordinaten der Bezeichnung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**LVGGR \_ SUBSETLINK**</dt> </dl> | Nur Koordinaten des Teilmengenlinks (Markupteilmenge). Ein Listenansicht-Steuerelement kann die Anzahl der sichtbaren Elemente begrenzen, die in jeder Gruppe angezeigt werden. Dem Benutzer wird ein Link angezeigt, damit der Benutzer die Gruppe erweitern kann. Dieses Flag gibt das umgebundene Rechteck des Teilmengenlinks zurück, wenn die Gruppe eine Teilmenge ist (Gruppenzustand von LVGS \_ SUBSETED, siehe Struktur [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **Memberzustand**). Dieses Flag wird bereitgestellt, damit Barrierefreiheitsanwendungen den Link finden können.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

