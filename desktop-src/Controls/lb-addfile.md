---
title: LB_ADDFILE Meldung (Winuser.h)
description: Fügt einem Listenfeld, das eine Verzeichnisauflistung enthält, den angegebenen Dateinamen hinzu.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bda3015fef36d6383f37f272ddaf25469fcb6930bb38bd0fa8122efc5b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434480"
---
# <a name="lb_addfile-message"></a>LB \_ ADDFILE-Meldung

Fügt einem Listenfeld, das eine Verzeichnisauflistung enthält, den angegebenen Dateinamen hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Namen der hinzuzufügenden Datei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der nullbasierte Index der hinzugefügten Datei oder LB \_ ERR, wenn ein Fehler auftritt.

## <a name="remarks"></a>Hinweise

Das Listenfeld, dem *lParam* hinzugefügt wird, muss von der [**DlgDirList-Funktion**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) ausgefüllt worden sein.

Die [**LB \_ INITSTORAGE-Nachricht**](lb-initstorage.md) beschleunigt die Initialisierung von Listenfeldern mit einer großen Anzahl von Elementen (mehr als 100). Sie reserviert die angegebene Arbeitsspeichermenge, sodass nachfolgende **\_ LB ADDFILE-Nachrichten** die kürzeste Zeit in Anspruch nehmen. Sie können Schätzungen für die *Parameter wParam* und *lParam* verwenden. Wenn Sie überbewerten, wird der zusätzliche Arbeitsspeicher belegt. Wenn Sie dies nicht möchten, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

Bei einer ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mit CP ACP in \_ Unicode. Dies kann Probleme verursachen. Beispielsweise werden romanische Zeichen mit Akzent in einem Nicht-Unicode-Listenfeld in japanischen Windows garniert angezeigt. Kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld, um dieses Problem zu beheben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> </dl>

 

 





