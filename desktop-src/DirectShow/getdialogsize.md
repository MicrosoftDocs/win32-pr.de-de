---
description: Die getdialogsize-Funktion Ruft die Größe eines Ressourcen Dialogfelds ab.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Getdialogsize-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371455"
---
# <a name="getdialogsize-function"></a>Getdialogsize-Funktion

Die **getdialogsize** -Funktion Ruft die Größe eines Ressourcen Dialogfelds ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iResourceID* 
</dt> <dd>

Der Ressourcen Bezeichner des Dialog Felds.

</dd> <dt>

*pdlgproc* 
</dt> <dd>

Zeiger auf die Dialogfeld Prozedur.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert, der in der "WM \_ InitDialog"-Meldung übergeben wird, die nach der Erstellung an das temporäre Dialogfeld gesendet wurde.

</dd> <dt>

*pResult* 
</dt> <dd>

Ein Zeiger auf eine **Größen** Struktur, die die Abmessungen des Dialog Felds in Bildschirm Pixel empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Dialogfeld Ressource gefunden wurde, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Eigenschaften Seiten können diese Funktion verwenden, um die tatsächliche Anzeige Größe zurückzugeben, die Sie benötigen. Die meisten Eigenschaften Seiten sind Dialogfelder und verfügen daher über Dialogfeld Vorlagen, die in Ressourcen Dateien gespeichert werden. Vorlagen verwenden Dialogfeld Einheiten, die nicht direkt auf Bildschirm Pixel zugeordnet werden. Allerdings muss die [**GetPageInfo**](cbasepropertypage-getpageinfo.md) -Funktion einer Eigenschaften Seite die tatsächliche Anzeige Größe in Pixel zurückgeben. Die Eigenschaften Seite kann aufrufen `GetDialogSize` , um die Anzeige Größe zu berechnen.

Diese Funktion erstellt eine temporäre Instanz des Dialog Felds. Um zu vermeiden, dass das Dialogfeld auf dem Bildschirm angezeigt wird, sollte die Dialogfeld Vorlage in der Ressourcen Datei nicht über eine Eigenschaft vom Typ "WS Visible" verfügen \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsfunktionen für Eigenschaften Seiten](property-page-helper-functions.md)
</dt> </dl>

 

 




