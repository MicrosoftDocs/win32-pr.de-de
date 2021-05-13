---
description: Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf. Ruft optional ein Element aus der -Enumeration ab.
title: EnumMRUListW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 1e6e4bd0820d35fec2a108a81eb1030567493e6a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843161"
---
# <a name="enummrulistw-function"></a>EnumMRUListW-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein. \]

Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf. Ruft optional ein Element aus der -Enumeration ab.

## <a name="syntax"></a>Syntax


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMRU* \[ In\]
</dt> <dd>

Typ: **HANDLE**

Das Handle der MRU-Liste, das beim Erstellen der Liste abgerufen wurde.

</dd> <dt>

*nItem* \[ In\]
</dt> <dd>

Typ: **int**

Das zurückzugebende Element. Wenn dieser Wert kleiner als 0 ist, gibt die Funktion die Anzahl der Elemente in der MRU-Liste zurück.

</dd> <dt>

*lpData* \[ out\]
</dt> <dd>

Typ: **\* void**

Ein Zeiger auf einen Puffer, der das in *nItem* angeforderte Element empfängt. Wenn *nItem* kleiner als 0 ist, bleibt der Inhalt dieses Puffers unverändert.

</dd> <dt>

*uLen* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des Puffers, einschließlich des beendenden NULL-Zeichens. Wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde, ist dies die Größe in Bytes. Andernfalls ist dies die Größe in Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt einen der folgenden Werte zurück.

-   Gibt die Anzahl der Elemente in der Enumeration zurück, wenn *nItem* kleiner als 0 ist.
-   Gibt -1 zurück, wenn ein Fehler aufgetreten ist.
-   Andernfalls gibt die Größe der in *lpData* zurückgegebenen Zeichenfolge zurück, einschließlich des beendenden NULL-Zeichens. Wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde, ist dies die Größe in Bytes. Andernfalls ist dies die Größe in Zeichen.

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten. Auf sie kann über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) zugegriffen oder aus comctl32.dll durch ihre Ordnungszahl extrahiert werden, d. h. 403 für **EnumMRUListW.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **EnumMRUListW** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
