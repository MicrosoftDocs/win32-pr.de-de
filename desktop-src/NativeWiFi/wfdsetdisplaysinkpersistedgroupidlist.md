---
description: Legt die Liste der beibehaltenen Gruppen-IDs für alle Profile fest, die von Ihrer APP persistent gespeichert werden.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Wfddisplaysink setpersistedgroupidlist-Funktion (wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347047"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a>Wfddisplaysink setpersistedgroupidlist-Funktion

Legt die Liste der beibehaltenen Gruppen-IDs für alle Profile fest, die von Ihrer APP persistent gespeichert werden. Ihre APP sollte diese Methode jedes Mal aufgerufen werden, wenn Sie ein Profil aus dem Speicher hinzufügt oder löscht.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cgroupidlist* \[ in\]
</dt> <dd>

Die Anzahl der Gruppen-IDs, auf die von *pgroupidlist* verwiesen wird.

</dd> <dt>

*pgroupidlist* \[ in\]
</dt> <dd>

Zeiger auf ein Array aus *cgroupidlist* -Gruppen-IDs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

## <a name="remarks"></a>Bemerkungen

Es wird immer erwartet, dass diese Methode mit der gesamten Liste und nicht mit einer Teilmenge aufgerufen wird. Es ist in Ordnung, diese Methode mit 0 Profilen aufzurufen, wenn der Profil Speicher leer ist.

Ein erneutes aufrufen für eine Gruppen-ID, die nicht Teil der angegebenen Liste ist, schlägt fehl mit "Fail; Unbekannte P2P-Gruppe "(Status 8).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wifdisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




