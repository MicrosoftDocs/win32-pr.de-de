---
description: Wählt eine Register-NIC aus.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Getnppblobfromui-Funktion (Netmon. h)
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
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960023"
---
# <a name="getnppblobfromui-function"></a>Getnppblobfromui-Funktion

Die **getnppblobfromui** -Funktion wählt eine Register-NIC aus.

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

*HWND* \[ in\]
</dt> <dd>

Ein Handle für ein Fenster, das das Dialogfeld " **Netzwerk auswählen** " anzeigt.

</dd> <dt>

*hfilterblob* \[ in\]
</dt> <dd>

Ein Handle für ein [*filterblob*](f.md) , das verwendet wird, um einzuschränken, welche NICs angezeigt werden.

</dd> <dt>

*phblob* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das Handle des BLOBs, das die ausgewählte NIC darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (der Benutzer wählt eine NIC aus), ist der Rückgabewert nmerr \_ Success, und das BLOB, auf das *phblob* verweist, wird ausgefüllt.

Wenn der Benutzer keine NIC auswählt, wird der Rückgabewert **nmerr \_ No \_ NPP \_ ausgewählt**.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein weiterer nmerr-Wert.

## <a name="remarks"></a>Bemerkungen

Wenn Sie aufgerufen wird, zeigt Netzwerkmonitor das Dialogfeld **Netzwerk auswählen** an, mit dem Sie eine NIC auswählen können. Das NPP-BLOB, das die NIC darstellt, wird an die aufrufenden Anwendung zurückgegeben.

Wenn das von *hfilterblob* benannte BLOB ein [*spezielles BLOB*](s.md)ist, versucht der Finder, es zu verarbeiten. Ein Beispiel wäre ein-Befehl, der zuvor ein spezielles BLOB von der Remote-NPP zurückgegeben hat. Die Anwendung hat das erforderliche Tag, den Computernamen, eingefügt \_ . In dieser Situation übergibt der Finder dieses BLOB an den NPP-Remote Computer, der dann eine Tabelle mit NPP-BLOBs zurückgibt, die den angeforderten Computer darstellen. Diese NPP-Remote-Blobfelder werden im Dialogfeld angezeigt.

Der Aufrufer muss die [destroyblob](destroyblob.md) -Funktion aufzurufen, die das zurückgegebene BLOB zerstört, wenn es nicht mehr benötigt wird.



| Weitere Informationen über | Siehe                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Drei Möglichkeiten zum Auswählen von NICs  | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |
| Angeben eines filterblobs   | [Angeben eines filterblobs](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Getnppblobtable](getnppblobtable.md)
</dt> <dt>

[Selectnppblobfromtable](selectnppblobfromtable.md)
</dt> </dl>

 

 




