---
description: Ruft die Quelladresse eines Frames ab.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: GetFrameSourceAddress-Funktion (Netmon.h)
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
ms.openlocfilehash: 4878e08b8d8fb475c0da23d2ed765819fa14a10cd93140c791ed8603b1677584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366317"
---
# <a name="getframesourceaddress-function"></a>GetFrameSourceAddress-Funktion

Die **GetFrameSourceAddress-Funktion** ruft die Quelladresse eines Frames ab.

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

*hFrame* 
</dt> <dd>

Ein Handle für den Frame, auf den ein Zeiger verweisen soll.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Ein Rückgabepuffer, der die Framequellenadresse speichert.

</dd> <dt>

*Adresstyp* 
</dt> <dd>

Der Typ der gesuchten Adresse, z. B. ADDRESS \_ TYPE ETHERNET oder ADDRESS TYPE \_ \_ \_ IP.

</dd> <dt>

*Flags* 
</dt> <dd>

Die Flags, die zum Ändern der zurückgegebenen Quelladressendaten verwendet werden.



| Wert                                                                                                                                                                                                           | Bedeutung                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**\_ADDRESSTYPE-FLAGS \_ NORMALISIEREN**</dt> </dl>        | Bricht die Routing- und Gruppen-BITs ab.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**ADDRESSTYPE \_ FLAGS \_ BIT \_ REVERSE**</dt> </dl> | Konvertiert Tokenring-Netzwerkadressen wieder in den normalen Zustand.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist *der lpAddress-Wert* gültig, und der Rückgabewert ist BHERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                                | Beschreibung                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_BHERR-PROTOKOLL \_ NICHT \_ GEFUNDEN**</dt> </dl> | Das durch den *AddressType-Parameter angegebene* Protokoll ist für den Frame ungültig.<br/> |
| <dl> <dt>**UNGÜLTIGER \_ \_ BHERR-HFRAME**</dt> </dl>      | Der *hFrame-Parameterwert* ist ungültig.<br/>                                        |



 

## <a name="remarks"></a>Hinweise

Der Adresstyp **ADDRESS TYPE FIND \_ \_ \_ HIGHEST** ist zulässig. Wenn dieser Adresstyp verwendet wird, sucht die Funktion nach der IPX-, XNS-, IP- oder VINES-IP-Adresse, bevor die ETHERNET-, TOKENRING- oder FDDI-Adresse zurückgegeben wird. Dieser Ansatz ist nützlich für Protokolle und Umgebungen, in denen zwei NICs unter einer einzelnen Serveradresse multiplexiert werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




