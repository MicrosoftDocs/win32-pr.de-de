---
description: Konvertiert die angegebenen Attributdaten in das XML-Format.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: Sdbformatattribute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860558"
---
# <a name="sdbformatattribute-function"></a>Sdbformatattribute-Funktion

Konvertiert die angegebenen Attributdaten in das XML-Format.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pattrinfo* \[ in\]
</dt> <dd>

Eine [**attrinfo**](attrinfo.md) -Struktur.

</dd> <dt>

*pchBuffer* \[ vorgenommen\]
</dt> <dd>

Der Ausgabepuffer.

</dd> <dt>

*dwbuffersize* \[ in\]
</dt> <dd>

Die Größe des *pchBuffer* -Puffers in Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt bei Erfolg **true** oder **false** zurück, wenn der Puffer zu klein ist oder das Attribut nicht gefunden wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbgetfileattribute**](sdbgetfileattributes.md)
</dt> </dl>

 

 




