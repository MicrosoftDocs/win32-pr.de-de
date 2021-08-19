---
description: Ruft einen Fehlercodebezeichner (Error Code Identifier, IDA) ab und erstellt die endgültige Anzeigezeichenfolge, wenn ein Jet-Fehler und erweiterte Fehlerinformationen bereitgestellt werden.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8b0fa6eb0ac4bc29e5657d3e58d9be1c27188a0faf7c7d68281ceca239dea8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955779"
---
# <a name="jeterrformattedmessage-function"></a>JetErrFormattedMessage-Funktion

Ruft einen Fehlercodebezeichner (Error Code Identifier, IDA) ab und erstellt die endgültige Anzeigezeichenfolge, wenn ein Jet-Fehler und erweiterte Fehlerinformationen bereitgestellt werden.

## <a name="syntax"></a>Syntax


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Err* 
</dt> <dd>

Die Jet-Fehlernummer, die zum Suchen und Formatieren der angezeigten Fehlermeldung verwendet wird.

</dd> <dt>

*pExtendedErrorInfo* 
</dt> <dd>

Alle Jet-Fehlerinformationen, einschließlich des Datenbanknamens, des Tabellennamens und aller kleineren Fehlerinformationen.

</dd> <dt>

*Pida* 
</dt> <dd>

Ein Zeiger auf die IDA, die dem spezifischen Fehlercode zugeordnet ist.

</dd> <dt>

*pMessage* 
</dt> <dd>

Ein Zeiger auf die Fehlermeldung.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Die Anzahl der Bytes in der Fehlermeldung.

</dd> <dt>

*–actual* 
</dt> <dd>

Ein Zeiger auf die tatsächliche Anzahl gelesener Bytes.

</dd> <dt>

*pContextId* 
</dt> <dd>

Ein Zeiger auf den Kontextbezeichner, der der Hilfedatei zugeordnet ist.

</dd> <dt>

*pwszHelp/file* 
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Datei, die den Fehler erklärt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie **JET \_ errSuccess** zurück. Andernfalls wird eine formatierte Fehlermeldung zurückgegeben, die den spezifischen Grund für den Fehler angibt.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
