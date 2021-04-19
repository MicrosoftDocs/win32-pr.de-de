---
description: Ruft die Quelladresse eines Frames ab.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Getframesourceaddress-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343253"
---
# <a name="getframesourceaddress-function"></a>Getframesourceaddress-Funktion

Die **getframesourceaddress** -Funktion Ruft die Quelladresse eines Frames ab.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameSourceAddress(
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

Ein Handle für den Frame, auf den ein Zeiger zu erhalten ist.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Ein Rückgabe Puffer, in dem die Frame Quelladresse gespeichert wird.

</dd> <dt>

*Adresstyp* 
</dt> <dd>

Der Typ der Adresse, nach der gesucht wird, \_ z \_ . b. adrestyp Ethernet oder \_ Adresstyp \_ -IP.

</dd> <dt>

*Flags* 
</dt> <dd>

Die Flags, die zum Ändern der zurückgegebenen Quell Adressdaten verwendet werden.



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
| <dl> <dt>**bHerr- \_ Protokoll \_ nicht \_ gefunden**</dt> </dl> | Das vom *adressstype* -Parameter angegebene Protokoll ist für den Frame ungültig.<br/> |
| <dl> <dt>**bWer hat einen \_ ungültigen \_ hframe**</dt> </dl>      | Der Wert des *hframe* -Parameters ist ungültig.<br/>                                        |



 

## <a name="remarks"></a>Bemerkungen

Es ist ein Adresstyp vom Typ " **Address \_ Type \_ Find \_ Best** " zulässig. Wenn dieser Adresstyp verwendet wird, sucht die-Funktion nach der IP-Adresse von IPX, xns, IP oder Vines, bevor die Ethernet-, TokenRing-oder die f-di-Adresse zurückgegeben wird. Diese Vorgehensweise ist nützlich für Protokolle und Umgebungen, in denen zwei NICs unter einer einzelnen Server Adresse multiplext werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




