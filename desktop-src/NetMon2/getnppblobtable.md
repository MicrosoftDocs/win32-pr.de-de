---
description: Die getnppblobtable-Funktion Ruft eine NPP-BLOB-Tabelle ab, die die Register-NICs auf dem lokalen Computer darstellt.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Getnppblobtable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866267"
---
# <a name="getnppblobtable-function"></a>Getnppblobtable-Funktion

Die **getnppblobtable** -Funktion Ruft eine NPP-BLOB-Tabelle ab, die die Register-NICs auf dem lokalen Computer darstellt.

## <a name="syntax"></a>Syntax


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hfilterblob* \[ in\]
</dt> <dd>

Handle für ein filterblob, das die in der Tabelle zurückgegebenen NPP-BLOBs einschränkt.

</dd> <dt>

*ppblobtable* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [BLOB- \_ Tabellen](blob-table.md) Struktur, die mindestens einen BLOB-Zeiger enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                | Beschreibung                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ keine \_ NPP- \_ dll**</dt> </dl>         | Es wurden keine DLLs im NPP-Verzeichnis gefunden.<br/>                    |
| <dl> <dt>**nmerr \_ keine \_ gültigen \_ NPP- \_ DLLs**</dt> </dl> | Keine der DLLs im NPP-Verzeichnis waren gültige NPP-DLLs.<br/>  |
| <dl> <dt>**nmerr \_ keine \_ übereinstimmenden \_ NPPs**</dt> </dl>   | Es wurden NPP-BLOB ermittelt, aber der Filter Test wurde nicht erfolgreich durchgeführt.<br/> |
| <dl> <dt>**nmerr \_ \_ von \_ Memor**</dt> </dl>       | Netzwerkmonitor konnte keinen Arbeitsspeicher zuordnen.<br/>            |



 

## <a name="remarks"></a>Bemerkungen

Das von *hfilterblob* benannte BLOB kann auch ein spezielles BLOB sein.

Wenn Sie das-Flag im filterblob auf **true** festlegen, kann die zurückgegebene BLOB-Tabelle auch spezielle BLOBs enthalten.

Wenn das von *hfilterblob* benannte BLOB ein spezielles BLOB ist, wird die Netzwerkmonitor-Benutzeroberfläche versuchen, Sie zu verarbeiten. Nehmen wir beispielsweise an, dass ein vorheriger-Rückruf ein spezielles BLOB aus dem Remote-NPP zurückgibt. Die Anwendung fügt das erforderliche Tag, den Computernamen, ein \_ . Der Finder übergibt dann dieses BLOB an den NPP-Remote Computer, der dann eine Tabelle mit den NPP-BLOBs zurückgibt, die dem Computernamen zugeordnet sind.

Um alle zurückgegebenen BLOBs und die BLOB-Tabelle zu zerstören, ist der Aufrufer für den Aufruf der **destroyblob** -Funktion verantwortlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




