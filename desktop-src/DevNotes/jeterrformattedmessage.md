---
description: Ruft einen Fehlercode Bezeichner (IDA) ab und erstellt die endgültige Anzeige Zeichenfolge, wenn ein Jet-Fehler und erweiterte Fehlerinformationen bereitgestellt werden.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Jeterrformattedmessage-Funktion
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
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369381"
---
# <a name="jeterrformattedmessage-function"></a>Jeterrformattedmessage-Funktion

Ruft einen Fehlercode Bezeichner (IDA) ab und erstellt die endgültige Anzeige Zeichenfolge, wenn ein Jet-Fehler und erweiterte Fehlerinformationen bereitgestellt werden.

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

*irre* 
</dt> <dd>

Die Jet-Fehlernummer, die verwendet wird, um die anzeigbare Fehlermeldung zu suchen und zu formatieren.

</dd> <dt>

*pextendederrorinfo* 
</dt> <dd>

Alle Jet-Fehlerinformationen, einschließlich Datenbankname, Tabellenname und geringfügige Fehlerinformationen.

</dd> <dt>

*pida* 
</dt> <dd>

Ein Zeiger auf die IDA, die dem spezifischen Fehlercode zugeordnet ist.

</dd> <dt>

*pMessage* 
</dt> <dd>

Ein Zeiger auf die Fehlermeldung.

</dd> <dt>

*cbmessage* 
</dt> <dd>

Gibt die Anzahl der Bytes in der Fehlermeldung an.

</dd> <dt>

*pcbactual* 
</dt> <dd>

Ein Zeiger auf die tatsächliche Anzahl der gelesenen Bytes.

</dd> <dt>

*pcontextid* 
</dt> <dd>

Ein Zeiger auf den Kontext Bezeichner, der der Hilfedatei zugeordnet ist.

</dd> <dt>

*pwszhelp/Datei* 
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Datei, in der der Fehler erläutert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **Jet \_ errsuccess** zurück; andernfalls wird eine formatierte Fehlermeldung zurückgegeben, die die Ursache für den Fehler angibt.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
