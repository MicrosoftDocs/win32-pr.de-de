---
title: Autoconvertto
description: Gibt die automatische Konvertierung einer bestimmten Klasse von Objekten in eine neue Klasse von Objekten an.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Autoconvertto-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855184"
---
# <a name="autoconvertto"></a>Autoconvertto

Gibt die automatische Konvertierung einer bestimmten Klasse von Objekten in eine neue Klasse von Objekten an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der den Klassen Bezeichner des Objekts angibt, in das das angegebene Objekt oder die Klasse von Objekten konvertiert werden soll.

Dieser Schlüssel wird normalerweise zum automatischen Konvertieren von Dateien verwendet, die von einer älteren Version einer Anwendung erstellt wurden, in eine neuere Version der Anwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Oledoautoconvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**Olegetautoconvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**Olesetautoconvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




