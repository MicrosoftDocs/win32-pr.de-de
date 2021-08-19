---
description: Ruft eine unformatierte Meldungszeichenfolge ab, wenn ein Fehlercodebezeichner (Error Code Identifier, IDA) bereitgestellt wird.
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 39bd07b3ac75bed85ff26dd7f014420ebaca8be16d6f0195d40e9161c0905496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955759"
---
# <a name="jeterridarawmessage-function"></a>JetErrIDARawMessage-Funktion

Ruft eine unformatierte Meldungszeichenfolge ab, wenn ein Fehlercodebezeichner (Error Code Identifier, IDA) bereitgestellt wird.

## <a name="syntax"></a>Syntax


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ida* 
</dt> <dd>

Eine Zahl, die einem bestimmten Fehlercode zugeordnet ist und dem Benutzer angezeigt wird.

</dd> <dt>

*pMessage* 
</dt> <dd>

Ein Zeiger auf die Fehlermeldung.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Die Anzahl der Bytes in der Fehlermeldung.

</dd> <dt>

*actual* 
</dt> <dd>

Ein Zeiger auf die tatsächliche Anzahl der gelesenen Bytes.

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

Wenn die Funktion erfolgreich ausgeführt wird, wird **JET \_ errSuccess** zurückgegeben. Andernfalls wird eine unformatierte Meldung zurückgegeben, die den spezifischen Grund für den Fehler angibt.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
