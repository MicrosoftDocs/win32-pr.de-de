---
description: Die Funktion SelectNPPBlobFromTable wählt eine NIC aus einer angegebenen NPP-BLOB-Tabelle aus.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: SelectNPPBlobFromTable-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14d9ca14d027efc1540f5a5d2ae78e948da68dd59247252989b617d07229bb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074410"
---
# <a name="selectnppblobfromtable-function"></a>SelectNPPBlobFromTable-Funktion

Die **Funktion SelectNPPBlobFromTable** wählt eine NIC aus einer angegebenen NPP-BLOB-Tabelle aus.

## <a name="syntax"></a>Syntax


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Behandeln Sie das Fenster, in dem das Dialogfeld **Netzwerk auswählen** angezeigt wird.

</dd> <dt>

*pBlobTable* \[ In\]
</dt> <dd>

Zeiger auf die angegebene BLOB-Tabelle. Netzwerkmonitor verwendet diese Tabelle, um das Dialogfeld **Netzwerk auswählen** aufzufüllen.

</dd> <dt>

*hBlob* \[ out\]
</dt> <dd>

Handle für das BLOB, das die ausgewählte NIC darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist und der Benutzer eine NIC auswählt, lautet der Rückgabewert NMERR \_ SUCCESS. Das BLOB, auf das *hBlob* zeigt, wird ausgefüllt.

Wenn der Benutzer keine NIC auswählt, lautet der Rückgabewert NMERR \_ NO \_ NPP \_ SELECTED.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein anderer NMERR-Wert.

## <a name="remarks"></a>Hinweise

Wenn sie aufgerufen wird, zeigt Netzwerkmonitor das Dialogfeld **Netzwerk auswählen** an, mit dem Sie eine NIC auswählen können. Das NPP-BLOB, das die ausgewählte NIC darstellt, kehrt zur aufrufenden Anwendung zurück.

Informationen zu den verschiedenen Möglichkeiten zum Auswählen von NETZWERKKARTEN finden Sie unter [Auswählen einer Netzwerkschnittstellenkarte.](selecting-a-network-interface-card.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Spezielle BLOB-Einträge](special-blob-entries.md)
</dt> </dl>

 

 




