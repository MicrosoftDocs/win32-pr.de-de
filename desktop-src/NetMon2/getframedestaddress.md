---
description: Ruft die Zieladresse eines Frames ab.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: GetFrameDestAddress-Funktion (Netmon.h)
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
ms.openlocfilehash: d7719392794027567521ce3e9c1bd1caf8ecbf76110f76ad0e54e0dd6549aae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366625"
---
# <a name="getframedestaddress-function"></a>GetFrameDestAddress-Funktion

Die **GetFrameDestAddress-Funktion** ruft die Zieladresse eines Frames ab.

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

*hFrame* 
</dt> <dd>

Ein Handle des Frames, auf den ein Zeiger angezeigt werden soll.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Ein Rückgabepuffer, in dem die Zieladresse des Frames gespeichert wird.

</dd> <dt>

*Adresstyp* 
</dt> <dd>

Ein Adresstyp, z. B. ADDRESS \_ TYPE ETHERNET oder ADDRESS TYPE \_ \_ \_ IP.

</dd> <dt>

*Flags* 
</dt> <dd>

Die Flags, die zum Ändern der zurückgegebenen Zieladressdaten verwendet werden.



| Wert                                                                                                                                                                                                           | Bedeutung                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**\_ADDRESSTYPE-FLAGS \_ NORMALISIEREN**</dt> </dl>        | Bricht die Routing- und Gruppen-BITs ab.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**ADDRESSTYPE \_ FLAGS \_ BIT \_ REVERSE**</dt> </dl> | Konvertiert Tokenringnetzwerkadressen wieder in den normalen Modus.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der *lpAddress-Wert* gültig, und der Rückgabewert ist BHERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                                | Beschreibung                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_BHERR-PROTOKOLL \_ NICHT \_ GEFUNDEN**</dt> </dl> | Das angegebene Protokoll im *AddressType-Parameter* ist für den Frame ungültig.<br/> |
| <dl> <dt>**BHERR \_ INVALID \_ HFRAME**</dt> </dl>      | Der *hFrame-Wert* ist ungültig.<br/>                                                  |



 

## <a name="remarks"></a>Hinweise

Der **\_ Adresstyp ADDRESS TYPE \_ FIND \_ HIGHEST** ist zulässig. Wenn dieser Adresstyp verwendet wird, sucht die Funktion nach der IPX-, XNS-, IP- oder VINES-IP-Adresse, bevor die ETHERNET-, TOKENRING- oder FDDI-Adresse zurückgegeben wird. Dieser Ansatz ist nützlich für Protokolle und in Umgebungen, in denen zwei NICs unter einer einzelnen Serveradresse multiplexiert werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




