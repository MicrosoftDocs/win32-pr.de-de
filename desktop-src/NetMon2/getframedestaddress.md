---
description: Ruft die Zieladresse eines Frames ab.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Getframedebug-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958721"
---
# <a name="getframedestaddress-function"></a>Getframedebug-Funktion

Die **getframedebug** -Funktion Ruft die Zieladresse eines Frames ab.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* 
</dt> <dd>

Ein Handle des Frames, auf den ein Zeiger angezeigt werden soll.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Ein Rückgabe Puffer, in dem die Frame Zieladresse gespeichert wird.

</dd> <dt>

*Adresstyp* 
</dt> <dd>

Eine Art Adresse, z \_ . b. adrestyp \_ Ethernet oder \_ Adresstyp \_ -IP.

</dd> <dt>

*Flags* 
</dt> <dd>

Die Flags, die zum Ändern der zurückgegebenen Ziel Adressdaten verwendet werden.



| Wert                                                                                                                                                                                                           | Bedeutung                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**adressstype- \_ Flags \_ normalisieren**</dt> </dl>        | Bricht die Routing-und Gruppen Bits ab.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**adressstype- \_ Flags \_ Bit \_ umkehren**</dt> </dl> | Konvertiert die Netzwerkadressen des tokenrings wieder in den normalen Zustand.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der *lpAddress* -Wert gültig, und der Rückgabewert ist bHerrn \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                                | Beschreibung                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**bHerr- \_ Protokoll \_ nicht \_ gefunden**</dt> </dl> | Das angegebene Protokoll im *Adresstype* -Parameter ist für den Frame ungültig.<br/> |
| <dl> <dt>**bWer hat einen \_ ungültigen \_ hframe**</dt> </dl>      | Der *hframe* -Wert ist ungültig.<br/>                                                  |



 

## <a name="remarks"></a>Bemerkungen

Der **\_ adrestyp " \_ Suche nach \_ höchster** Adresse" ist zulässig. Wenn dieser Adresstyp verwendet wird, sucht die-Funktion nach der IP-Adresse von IPX, xns, IP oder Vines, bevor die Ethernet-, TokenRing-oder die f-di-Adresse zurückgegeben wird. Diese Vorgehensweise ist nützlich für Protokolle und in Umgebungen, in denen zwei NICs unter einer einzelnen Server Adresse multiplext werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




