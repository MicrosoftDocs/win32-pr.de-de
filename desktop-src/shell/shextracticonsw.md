---
description: Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert werden.
title: Shextractiensw-Funktion
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
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994806"
---
# <a name="shextracticonsw-function"></a>Shextractiensw-Funktion

\[**Shextractitsw** ist über Windows XP Service Pack 2 (SP2) verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.\]

Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert werden.

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

*pszFileName* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf den Dateinamen, aus dem die Symbole extrahiert werden sollen.

</dd> <dt>

*nidindex* \[ in\]
</dt> <dd>

Typ: **int**

Der Index des ersten Symbols, das aus der in *pszFileName* benannten Ressource extrahiert werden soll.

</dd> <dt>

*cxicon* \[ in\]
</dt> <dd>

Typ: **int**

Die gewünschte Breite des Symbols. Siehe Hinweise.

</dd> <dt>

*cyicon* \[ in\]
</dt> <dd>

Typ: **int**

Die gewünschte Höhe des Symbols. Siehe Hinweise.

</dd> <dt>

*phicon* \[ vorgenommen\]
</dt> <dd>

Typ: **HICON \** _

Diese Funktion gibt einen Zeiger auf das Array von Symbol Handles zurück.

</dd> <dt>

_pIconId * \[ out\]
</dt> <dd>

Typ: **uint \** _

Wenn diese Funktion zurückgegeben wird, enthält Sie einen Zeiger auf den Ressourcen Bezeichner des extrahierten Symbols, das am besten zum aktuellen Anzeigegerät passt. Wenn kein Bezeichner für dieses Format verfügbar ist, enthält er "0xffffffff". Wenn kein Bezeichner aus einem anderen Grund abgerufen werden kann, gibt 0 (null) zurück.

</dd> <dt>

_nIcons * \[ in\]
</dt> <dd>

Typ: **uint**

Die Anzahl der Symbole, die aus der in *pszFileName* benannten Ressource extrahiert werden sollen. Dieser Parameter ist nur gültig, wenn es sich bei der Ressource um eine exe-oder DLL-Datei handelt.

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Typ: **uint**

Die Flags, die diese Funktion steuern. Mögliche Werte finden Sie unter dem *fuload* -Parameter der [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) -Funktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Ein Wert ungleich 0 (null), wenn erfolgreich; andernfalls 0 (null).

## <a name="remarks"></a>Bemerkungen

**Shextractikonsw** extrahiert aus den folgenden Dateitypen.

-   Ausführbare Datei (.exe)
-   Dll (dll)
-   Symbol (. ico)
-   Cursor (. cur)
-   Animierter Cursor (. ani)
-   Bitmap (.bmp)

Extraktionen von Windows 3. ausführbare *x* 16-Bit-Dateien (exe-oder DLL-Dateien) werden ebenfalls unterstützt.

Mit den Parametern *cxicon* und *cyicon* wird die Größe der zu extrahierenden Symbole angegeben. Sie können zwei Größen durch die einzelnen Parameter extrahieren, indem Sie den Wert zwischen seinem LoWord und HIWORD aufteilen. Legen Sie die erste gewünschte Größe in das lowort des-Parameters und die zweite Größe im HIWORD-Format ab. Beispielsweise extrahiert [**makelong**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) sowohl für *cxicon* als auch für *cyicon* sowohl 24-als auch 48-Symbole.

Der Aufrufprozess ist dafür verantwortlich, alle Symbole zu zerstören, die durch diese Funktion durch Aufrufen der [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) -Funktion extrahiert werden.

**Shextractiensw** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert. Um es zu verwenden, müssen Sie einen übereinstimmenden Prototyp deklarieren und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um einen Funktionszeiger von Shell32.dll anzufordern, der zum Aufrufen dieser Funktion verwendet werden kann.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Shextractitsw** (Unicode)<br/>                                                                      |



 

 
