---
description: Wählt eine Register-NIC aus.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: GetNPPBlobFromUI-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d3b88c369145d53d32d23773072f878d9834110e705cd8ff623a3726cbb98b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743880"
---
# <a name="getnppblobfromui-function"></a>GetNPPBlobFromUI-Funktion

Die **GetNPPBlobFromUI-Funktion** wählt eine Register-NIC aus.

## <a name="syntax"></a>Syntax


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Ein Handle für ein Fenster, in dem das **Dialogfeld Netzwerk auswählen** angezeigt wird.

</dd> <dt>

*hFilterBlob* \[ In\]
</dt> <dd>

Ein Handle für ein [*FilterBLOB,*](f.md) das verwendet wird, um zu begrenzen, welche NICs angezeigt werden.

</dd> <dt>

*phBlob* \[ out\]
</dt> <dd>

Ein Zeiger auf das Handle des BLOB, das die ausgewählte NIC darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (der Benutzer wählt eine NIC aus), ist der Rückgabewert NMERR SUCCESS, und das BLOB, auf das \_ *phBlob* zeigt, wird ausgefüllt.

Wenn der Benutzer keine NIC auswählt, ist der Rückgabewert **NMERR \_ NO \_ NPP \_ SELECTED.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein weiterer NMERR-Wert.

## <a name="remarks"></a>Hinweise

Wenn aufgerufen, Netzwerkmonitor das Dialogfeld Netzwerk **auswählen** angezeigt, mit dem Sie eine NIC auswählen können. Das NPP-BLOB, das die NIC darstellt, wird an die aufrufende Anwendung zurückgegeben.

Wenn das BLOB mit dem Namen *hFilterBlob* ein spezielles [*BLOB ist,*](s.md)versucht der Finder, es zu verarbeiten. Ein Beispiel wäre ein Aufruf, der zuvor ein spezielles BLOB vom Remote-NPP zurückgegeben hätte. Die Anwendung hat das erforderliche Tag MACHINE \_ NAME eingefügt. In diesem Fall würde der Finder dieses BLOB an das Remote-NPP übergeben, das dann eine Tabelle mit NPP-BLOBs zurückgeben würde, die den angeforderten Computer darstellen. Diese Remote-NPP-BLOBs werden im Dialogfeld angezeigt.

Der Aufrufer muss die [DestroyBlob-Funktion](destroyblob.md) aufrufen, die das zurückgegebene BLOB zerstört, wenn es nicht mehr benötigt wird.



| Weitere Informationen über | Siehe                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Drei Möglichkeiten zum Auswählen von Netzwerkkarten  | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |
| Angeben eines Filterblobs   | [Angeben eines FilterBLOBs](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SelectNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 




