---
title: AutoConvertTo
description: Gibt die automatische Konvertierung einer angegebenen Klasse von -Objekten in eine neue Klasse von -Objekten an.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- COM-Registrierungsschlüssel "AutoConvertTo"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ea2b32445bb7107dcbfdc2aec8aee518fdd474674e76fdbd820265d06b6160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097050"
---
# <a name="autoconvertto"></a>AutoConvertTo

Gibt die automatische Konvertierung einer angegebenen Klasse von -Objekten in eine neue Klasse von -Objekten an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert,** der den Klassenbezeichner des Objekts angibt, in das das gegebene Objekt oder die Klasse von Objekten konvertiert werden soll.

Dieser Schlüssel wird in der Regel verwendet, um Dateien, die von einer älteren Version einer Anwendung erstellt wurden, automatisch in eine neuere Version der Anwendung zu konvertieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




