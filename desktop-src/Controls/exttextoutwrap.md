---
title: Exttextoutwrap-Funktion
description: Zeichnet Text mithilfe der aktuell ausgewählten Schriftart, Hintergrundfarbe und Textfarbe. Optional können Sie Dimensionen angeben, die für das Abschneiden, die Deckkraft oder beides verwendet werden sollen. Diese Funktion umschließt einen exttextout-aufrufsausdruck.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Windows-Steuerelemente der exttextoutwrap-Funktion
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102978"
---
# <a name="exttextoutwrap-function"></a>Exttextoutwrap-Funktion

\[**Exttextoutwrap** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar. Es wird empfohlen, stattdessen [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) direkt zu verwenden.\]

Zeichnet Text mithilfe der aktuell ausgewählten Schriftart, Hintergrundfarbe und Textfarbe. Optional können Sie Dimensionen angeben, die für das Abschneiden, die Deckkraft oder beides verwendet werden sollen. Diese Funktion umschließt einen [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)-aufrufsausdruck.

## <a name="syntax"></a>Syntax


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ in\]
</dt> <dd>

Typ: **[ **hdc**](/windows/desktop/WinProg/windows-data-types)**

Ein Handle für den Gerätekontext.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Typ: **int**

Die x-Koordinate (in logischen Koordinaten) des Bezugspunkts, der zum Positionieren der Zeichenfolge verwendet wird.

</dd> <dt>

*J* \[ in\]
</dt> <dd>

Typ: **int**

Die y-Koordinate (in logischen Koordinaten) des Bezugspunkts, der zum Positionieren der Zeichenfolge verwendet wird.

</dd> <dt>

*uoptions* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Werte, die angeben, wie das Anwendungs definierte Rechteck verwendet werden soll. Eine umfassende Liste der Optionen finden [**Sie unter exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .

</dd> <dt>

*LPRC* \[ in\]
</dt> <dd>

Typ: * Konstante *[**Rect**](/previous-versions//dd162897(v=vs.85)) \** _

Ein Zeiger auf eine optionale [_ *Rect* *](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Dimensionen (in logischen Koordinaten) eines Rechtecks angibt, das für Clipping, Deckkraft oder beides verwendet wird.

</dd> <dt>

*lpString* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf einen Puffer, der den Text enthält, der gezeichnet werden soll. Die Zeichenfolge muss nicht mit 0 (null) beendet werden, da *cbcount* die Länge der Zeichenfolge angibt.

</dd> <dt>

*cbcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Länge der Zeichenfolge in Bytes, auf die von *lpString* verwiesen wird.

</dd> <dt>

*lpdx* \[ in\]
</dt> <dd>

Typ: * Konstante *[**int**](/windows/desktop/WinProg/windows-data-types) \** _

Ein Zeiger auf ein optionales Array von-Werten, die den Abstand zwischen den Ursprüngen der angrenzenden Zeichen Zellen angeben. Beispielsweise trennen _lpDx x \[ \] -Einheiten logische Einheiten die Ursprünge der Zeichen Zelle x und der Zeichen Zelle (x + 1).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Gibt einen Wert ungleich 0 (null) zurück, wenn die Zeichenfolge erfolgreich gezeichnet wird. Wenn die ANSI-Version von [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) jedoch mit dem Eto- \_ Glyphe-Index aufgerufen wird \_ , gibt die Funktion **true** zurück, auch wenn die Funktion keine Aktion ausführt.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**Exttextoutwrap** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 417 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.

Weitere Hinweise finden Sie unter [**exttextout**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 6,0 oder höher)</dt> </dl> |



 

