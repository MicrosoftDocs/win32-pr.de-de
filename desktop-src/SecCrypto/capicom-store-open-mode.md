---
description: Wird mit der Store. Open-Methode verwendet, um anzugeben, wie ein Zertifikat Speicher geöffnet werden soll.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: CAPICOM_STORE_OPEN_MODE-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359700"
---
# <a name="capicom_store_open_mode-enumeration"></a>CAPICOM \_ Store \_ - \_ Enumeration im öffnenden Modus

Der \_ \_ Enumerationstyp "CAPICOM Store Open \_ Mode" wird mit der [**Store. Open**](store-open.md) -Methode verwendet, um anzugeben, wie ein Zertifikat Speicher geöffnet werden soll.

## <a name="members"></a>Member



| Member                                      | BESCHREIBUNG                                                                                                                                                              | Wert |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ Store \_ Open \_ Read \_ Only**        | Öffnen Sie den Speicher im schreibgeschützten Modus.<br/>                                                                                                                             | 0     |
| **CAPICOM \_ Store \_ offene \_ Lese- \_ /Schreibzugriff**       | Öffnen Sie den Speicher im Lese-/Schreibmodus.<br/>                                                                                                                            | 1     |
| **\_ \_ \_ maximal zulässige Anzahl geöffneter CAPICOM-Speicher \_**  | Öffnen Sie den Speicher im Lese-/Schreibmodus, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Wenn der Benutzer nicht über Lese-/Schreibberechtigungen verfügt, öffnen Sie den Speicher im schreibgeschützten Modus.<br/> | 2     |
| **CAPICOM \_ - \_ Speicher \_ Öffnen \_ nur vorhanden**    | Nur vorhandene Speicher öffnen; Erstellen Sie keinen neuen Speicher. Eingeführt von CAPICOM 2,0.<br/>                                                                              | 128   |
| **CAPICOM \_ Store \_ Open \_ include \_ archiviert** | Schließt Archivierte Zertifikate ein, wenn der Speicher verwendet wird. Eingeführt von CAPICOM 2,0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Bemerkungen

Wenn Sie die Enumeration "CAPICOM \_ Store \_ Open Mode" verwenden \_ , kann nur eine der folgenden Einstellungen verwendet werden.

-   CAPICOM \_ Store \_ Open \_ Read \_ Only
-   CAPICOM \_ Store \_ offene \_ Lese- \_ /Schreibzugriff
-   \_ \_ \_ maximal zulässige Anzahl geöffneter CAPICOM-Speicher \_

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> </dl>

 

 




