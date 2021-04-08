---
title: Behandlungen
description: Gibt die CLSID einer Klasse an, die die aktuelle Klasse emulieren kann.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Registrierungsschlüssel für TreatAs com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856399"
---
# <a name="treatas"></a>Behandlungen

Gibt die CLSID einer Klasse an, die die aktuelle Klasse emulieren kann.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert.

Emulation ist die Fähigkeit einer Anwendung, ein Objekt einer anderen Klasse zu öffnen und zu bearbeiten, wobei das ursprüngliche Format des Objekts beibehalten wird. Die Lösung erfolgt auf dem lokalen Computer, sodass bei der Remote Aktivierung die Auflösung auf dem Client Computer unter Verwendung der von **TreatAs** angegebenen CLSID erfolgt.

DCOM prüft die lokale Registrierung für **TreatAs**, auch wenn Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen und einen Remote Server angeben. Dies bedeutet Folgendes: Wenn Sie einen **behandateneintrag** für Class1 haben, der auf dem lokalen Computer als Klasse2 behandelt werden soll, wenn Sie jedoch **cokreateinstance** aufrufen, um eine Instanz von Class1 zu erstellen und einen Remote Server anzugeben, versucht DCOM, eine Instanz von Klasse2 auf dem Remote Server zu erstellen, auch wenn Klasse2 nicht auf dem Remote Server registriert ist, was dazu führt, dass der **cokreateinstance** -Befehl fehlschlägt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AutoTreatAs**](autotreatas.md)
</dt> <dt>

[**Cogettreatasclass**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**Cotreatasclass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




