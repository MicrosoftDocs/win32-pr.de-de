---
description: Die OpenLog-Methode des Merge-Objekts öffnet eine Protokolldatei, die Status-und Fehlermeldungen empfängt. Wenn die Protokolldatei bereits vorhanden ist, fügt das Installationsprogramm neue Nachrichten an. Wenn die Protokolldatei nicht vorhanden ist, erstellt das Installationsprogramm eine Protokolldatei.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Merge. OpenLog-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370873"
---
# <a name="mergeopenlog-method"></a>Merge. OpenLog-Methode

Die **OpenLog** -Methode des [**Merge**](merge-object.md) -Objekts öffnet eine Protokolldatei, die Status-und Fehlermeldungen empfängt. Wenn die Protokolldatei bereits vorhanden ist, fügt das Installationsprogramm neue Nachrichten an. Wenn die Protokolldatei nicht vorhanden ist, erstellt das Installationsprogramm eine Protokolldatei.

## <a name="syntax"></a>Syntax


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Filename* 
</dt> <dd>

Voll qualifizierter Dateiname, der auf eine Datei verweist, die geöffnet oder erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Clients können Ihre eigenen Nachrichten über die [**Log**](merge-log.md) -Methode an diese Protokolldatei senden.

### <a name="c"></a>C++

Siehe [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
