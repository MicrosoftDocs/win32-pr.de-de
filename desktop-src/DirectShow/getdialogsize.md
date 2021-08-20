---
description: Die GetDialogSize-Funktion ruft die Größe eines Ressourcendialogfelds ab.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: GetDialogSize-Funktion (Wxutil.h)
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
ms.openlocfilehash: 7f1f2631e169549895a1f74ce571b2abfeeee8cd77ac7cb3c4dfc5aa6913a6d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564950"
---
# <a name="getdialogsize-function"></a>GetDialogSize-Funktion

Die **GetDialogSize-Funktion** ruft die Größe eines Ressourcendialogfelds ab.

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

Ressourcenbezeichner des Dialogfelds.

</dd> <dt>

*pDlgProc* 
</dt> <dd>

Zeiger auf die Dialogfeldprozedur.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert, der in der WM INITDIALOG-Nachricht übergeben wird, die direkt nach derEntarbeitung an das temporäre \_ Dialogfeld gesendet wird.

</dd> <dt>

*pResult* 
</dt> <dd>

Zeiger auf eine **SIZE-Struktur,** die die Dimensionen des Dialogfelds in Bildschirmpixeln empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Dialogfeldressource gefunden wurde, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Eigenschaftenseiten können mit dieser Funktion die tatsächliche Anzeigegröße zurückgeben, die sie benötigen. Die meisten Eigenschaftenseiten sind Dialogfelder und verfügen daher über Dialogfeldvorlagen, die in Ressourcendateien gespeichert sind. Vorlagen verwenden Dialogfeldeinheiten, die nicht direkt den Bildschirmpixeln zuordnen. Die [**GetPageInfo-Funktion**](cbasepropertypage-getpageinfo.md) einer Eigenschaftenseite muss jedoch die tatsächliche Anzeigegröße in Pixel zurückgeben. Die Eigenschaftenseite kann `GetDialogSize` aufrufen, um die Anzeigegröße zu berechnen.

Diese Funktion erstellt eine temporäre Instanz des Dialogfelds. Um zu vermeiden, dass das Dialogfeld auf dem Bildschirm angezeigt wird, sollte die Dialogfeldvorlage in der Ressourcendatei keine WS \_ VISIBLE-Eigenschaft haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsfunktionen für Eigenschaftenseiten](property-page-helper-functions.md)
</dt> </dl>

 

 




