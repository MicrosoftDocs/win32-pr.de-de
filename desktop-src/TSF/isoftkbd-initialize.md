---
title: ISOFT kbd Initialize-Methode (Software-BDC. h)
description: Die isoftkbd Initialize-Methode initialisiert alle erforderlichen Felder für eine weiche Tastatur und generiert standardmäßige weiche Tastaturlayouts.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Initialisieren der Methode Text Dienste-Framework
- Initialize Method Text Services Framework, iSOFT kbd Interface
- ISOFT kbd Interface Text Services-Framework, Initialize-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740208"
---
# <a name="isoftkbdinitialize-method"></a>ISOFT kbd:: Initialize-Methode

Die **isoftkbd:: Initialize** -Methode initialisiert alle notwendigen Felder für eine weiche Tastatur und generiert standardmäßige weiche Tastaturlayouts.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                | BESCHREIBUNG                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Software-Domänen Controller. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Software. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iweichkbd**](isoftkbd.md)
</dt> </dl>

 

 





