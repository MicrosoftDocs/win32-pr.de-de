---
description: Übergibt einen Schlüsselwert mit allen zugeordneten Daten, die vom Modul für die Inhalts Entschlüsselung für das angegebene Schlüsselsystem benötigt werden.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'IMF mediakeysession:: Update-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366375"
---
# <a name="imfmediakeysessionupdate-method"></a>IMF mediakeysession:: Update-Methode

Übergibt einen Schlüsselwert mit allen zugeordneten Daten, die vom Modul für die Inhalts Entschlüsselung für das angegebene Schlüsselsystem benötigt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* 
</dt> <dd></dd> <dt>

*betrieben* 
</dt> <dd>

Die Anzahl in Bytes des *Schlüssels*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF mediakeysession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




