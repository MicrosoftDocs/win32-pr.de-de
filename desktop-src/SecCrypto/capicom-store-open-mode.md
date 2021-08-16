---
description: Wird mit dem Store. Öffnen Sie die -Methode, um anzugeben, wie ein Zertifikatspeicher geöffnet werden soll.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: CAPICOM_STORE_OPEN_MODE -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ebd46b751f4a098361618f3b6e992e4333425f501bf6afdedfca047e921ad7ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772057"
---
# <a name="capicom_store_open_mode-enumeration"></a>CAPICOM \_ STORE \_ OPEN \_ MODE-Enumeration

Der CAPICOM \_ STORE \_ OPEN \_ MODE-Enumerationstyp wird mit dem [**Store. Öffnen Sie**](store-open.md) die -Methode, um anzugeben, wie ein Zertifikatspeicher geöffnet werden soll.

## <a name="members"></a>Member



| Member                                      | Beschreibung                                                                                                                                                              | Wert |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY**        | Öffnen Sie den Speicher im schreibgeschützten Modus.<br/>                                                                                                                             | 0     |
| **CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**       | Öffnen Sie den Speicher im Lese-/Schreibmodus.<br/>                                                                                                                            | 1     |
| **CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED**  | Öffnen Sie den Speicher im Lese-/Schreibmodus, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Wenn der Benutzer nicht über Lese-/Schreibberechtigungen verfügt, öffnen Sie den Speicher im schreibgeschützten Modus.<br/> | 2     |
| **CAPICOM \_ STORE \_ OPEN \_ EXISTING \_ ONLY**    | Nur vorhandene Speicher öffnen; erstellen Sie keinen neuen Speicher. Eingeführt von CAPICOM 2.0.<br/>                                                                              | 128   |
| **CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED** | Schließen Sie archivierte Zertifikate ein, wenn Sie den Speicher verwenden. Eingeführt von CAPICOM 2.0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Hinweise

Bei Verwendung der CAPICOM \_ STORE \_ OPEN \_ MODE-Enumeration kann nur eine der folgenden Einstellungen verwendet werden.

-   CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY
-   CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE
-   CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Store. Öffnen**](store-open.md)
</dt> </dl>

 

 




