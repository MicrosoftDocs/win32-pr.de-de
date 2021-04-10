---
title: CQPM_PERSIST Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seite Abfrage Daten aus persistenten Speicher lesen oder schreiben kann.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- CQPM_PERSIST Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040551"
---
# <a name="cqpm_persist-message"></a>Cqpm- \_ persistenznachricht

Die **cqpm \_ -persistenznachricht** wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seite Abfrage Daten aus persistenten Speicher lesen oder schreiben kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält einen Wert ungleich 0, um die Abfrage Daten zu lesen, oder NULL, um die Abfrage Daten zu schreiben.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ipersistquery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) -Schnittstelle, von der die Abfrage Daten gelesen oder geschrieben werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** oder andernfalls einen Standard- **HRESULT** -Fehlercode zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**Ipersistquery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

