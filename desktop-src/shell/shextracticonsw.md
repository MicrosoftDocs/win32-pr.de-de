---
description: Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert wurden.
title: SHExtractIconsW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840911"
---
# <a name="shextracticonsw-function"></a>SHExtractIconsW-Funktion

\[**SHExtractIconsW** ist über Windows XP Service Pack 2 (SP2) verfügbar. Sie kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]

Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert wurden.

## <a name="syntax"></a>Syntax


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszFileName* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf den Dateinamen, aus dem die Symbole extrahiert werden sollen.

</dd> <dt>

*nIconIndex* \[ In\]
</dt> <dd>

Typ: **int**

Der Index des ersten Symbols, das aus der Ressource namens in *pszFileName* extrahiert werden soll.

</dd> <dt>

*cxIcon* \[ In\]
</dt> <dd>

Typ: **int**

Die gewünschte Breite des Symbols. Siehe Hinweise.

</dd> <dt>

*cyIcon* \[ In\]
</dt> <dd>

Typ: **int**

Die gewünschte Höhe des Symbols. Siehe Hinweise.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Typ: **HICON \***

Enthält nach der Rückkehr dieser Funktion einen Zeiger auf das Array von Symbolhandles.

</dd> <dt>

*pIconId* \[ out\]
</dt> <dd>

Typ: **UINT \***

Wenn diese Funktion zurückgegeben wird, enthält sie einen Zeiger auf den Ressourcenbezeichner des extrahierten Symbols, das am besten zum aktuellen Anzeigegerät passt. Wenn für dieses Format kein Bezeichner verfügbar ist, enthält es 0xFFFFFFFF. Wenn aus einem anderen Grund kein Bezeichner erhalten werden kann, gibt 0 (null) zurück.

</dd> <dt>

*nIcons* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Anzahl der Symbole, die aus der Ressource mit dem Namen in *pszFileName extrahiert werden.* Dieser Parameter ist nur gültig, wenn die Ressource eine EXE- oder DLL-Datei ist.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Flags, die diese Funktion steuern. Mögliche Werte finden Sie unter *dem fuLoad-Parameter* der [**LoadImage-Funktion.**](/windows/win32/api/winuser/nf-winuser-loadimagea)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UINT**

Ein Wert ungleich 0 (null), wenn erfolgreich; andernfalls 0 (null).

## <a name="remarks"></a>Hinweise

**SHExtractIconsW** extrahiert aus den folgenden Dateitypen.

-   Ausführbare Datei (.exe)
-   DLL (.dll)
-   Symbol (.ico)
-   Cursor (.cur)
-   Animierter Cursor (.ani)
-   Bitmap (.bmp)

Extraktionen aus Windows 3. *x* ausführbare 16-Bit-Dateien (EXE oder DLL) werden ebenfalls unterstützt.

Die Parameter *cxIcon* und *cyIcon* geben die Größe der zu extrahierende Symbole an. Zwei Größen können über jeden Parameter extrahiert werden, indem der Wert zwischen LOWORD und HIWORD aufgeteilt wird. Legen Sie die erste gewünschte Größe in loword des Parameters und die zweite Größe in hiword ein. Beispielsweise extrahiert [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) sowohl für *cxIcon* als auch *für cyIcon* symbole mit einer Größe von 24 und 48.

Der aufrufende Prozess ist dafür verantwortlich, alle Über diese Funktion extrahierten Symbole zu zerstören, indem die [**DestroyIcon-Funktion**](/windows/win32/api/winuser/nf-winuser-destroyicon) aufgerufen wird.

**SHExtractIconsW** wird nicht anhand des Namens exportiert oder in einer öffentlichen Headerdatei deklariert. Um ihn zu verwenden, müssen Sie einen übereinstimmenden Prototyp deklarieren und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um einen Funktionszeiger von Shell32.dll anzufordern, der zum Aufrufen dieser Funktion verwendet werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SHExtractIconsW** (Unicode)<br/>                                                                      |



 

 
