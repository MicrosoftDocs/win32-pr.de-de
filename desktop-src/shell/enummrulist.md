---
description: Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf. Ruft optional ein Element aus der-Enumeration ab.
title: Enummrulistw-Funktion
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
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867748"
---
# <a name="enummrulistw-function"></a>Enummrulistw-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar. \]

Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf. Ruft optional ein Element aus der-Enumeration ab.

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

*hmru* \[ in\]
</dt> <dd>

Typ: **handle**

Das Handle der MRU-Liste, das beim Erstellen der Liste abgerufen wurde.

</dd> <dt>

*nitem* \[ in\]
</dt> <dd>

Typ: **int**

Das zurück zugebende Element. Wenn dieser Wert kleiner als 0 ist, gibt die Funktion die Anzahl der Elemente in der MRU-Liste zurück.

</dd> <dt>

*lpdata* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **void \** _

Ein Zeiger auf einen Puffer, der das in _nItem * angeforderte Element empfängt. Wenn *nitem* kleiner als 0 ist, ist der Inhalt dieses Puffers unverändert.

</dd> <dt>

*uLen* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des Puffers, einschließlich des abschließenden NULL-Zeichens. Wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde, ist dies die Größe in Bytes. Andernfalls ist es die Größe in Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt einen der folgenden Werte zurück.

-   Gibt die Anzahl der Elemente in der Enumeration zurück, wenn *nitem* kleiner als 0 (null) ist.
-   Gibt-1 zurück, wenn ein Fehler aufgetreten ist.
-   Andernfalls wird die Größe der in *lpdata* zurückgegebenen Zeichenfolge zurückgegeben, einschließlich des abschließenden NULL-Zeichens. Wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde, ist dies die Größe in Bytes. Andernfalls ist es die Größe in Zeichen.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten. Der Zugriff darauf erfolgt über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) oder das Extrahieren aus comctl32.dll durch die Ordnungszahl, die 403 für **enummrulistw** ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5,0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Enummrulistw** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"Kreatemrulistw"**](createmrulist.md)
</dt> <dt>

[**Mruinfo**](mruinfo.md)
</dt> </dl>

 

 
