---
description: Ruft das umgebende Rechteck der Windows-Taskleiste ab.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: ABM_GETTASKBARPOS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525430"
---
# <a name="abm_gettaskbarpos-message"></a>ABM \_ gettaskbarpos-Nachricht

Ruft das umgebende Rechteck der Windows-Taskleiste ab.


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, deren **RC** -Member das umschließende Rechteck (in Bildschirm Koordinaten) der Taskleiste empfängt. Beim Senden dieser Nachricht muss **CBSIZE** angegeben werden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass dies nur für die Taskleiste des Systems gilt. Andere Objekte, insbesondere Symbolleisten, die mit Software von Drittanbietern bereitgestellt werden, können auch vorhanden sein. Folglich sind einige der Bildschirmbereiche, die nicht von der Windows-Taskleiste abgedeckt werden, für den Benutzer möglicherweise nicht sichtbar. Verwenden Sie die [**getmonitorinfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) -Funktion, um den Bereich des Bildschirms abzurufen, der nicht von der Taskleiste und anderen APP-leisten für den Arbeitsbereich der Anwendung abgedeckt wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

