---
description: Die IWordInfo-Schnittstelle ist eine japanischspezifische Sprachressourcenkomponente. Das -Objekt analysiert Text und identifiziert einzelne Wörter und gibt entweder die Wörter in der Zeichenfolge zurück oder gibt die Wörterbuchformen (Stammformen) der Wörter im Text der Zeichenfolge zurück.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: IWordInfo-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: a82ff0c5d817dbec6d64d1d38d40245983877563416b30760926bb7522cd14c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001470"
---
# <a name="iwordinfo-interface"></a>IWordInfo-Schnittstelle

\[Diese Schnittstelle ist veraltet und wird auf Windows Vista nicht unterstützt.\]

Die **IWordInfo-Schnittstelle** ist eine japanischspezifische Sprachressourcenkomponente. Das -Objekt analysiert Text und identifiziert einzelne Wörter und gibt entweder die Wörter in der Zeichenfolge zurück oder gibt die Wörterbuchformen (Stammformen) der Wörter im Text der Zeichenfolge zurück.

## <a name="members"></a>Member

Die **IWordInfo-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWordInfo** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWordInfo-Schnittstelle** verfügt über diese Methoden.



| Methode        | BESCHREIBUNG                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | Analysiert Text, um Wörter zu identifizieren, und stellt die Ergebnisse für das [WordSink-Objekt](/previous-versions//ms691570(v=vs.85)) bereit.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wird verwendet, um japanische Wortumbrüche oder Wörterbuchformulare für den zu analysierenden Text abzurufen. Die Wörterbuchform eines Worts ist die unbeeindruckte Form des Worts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
