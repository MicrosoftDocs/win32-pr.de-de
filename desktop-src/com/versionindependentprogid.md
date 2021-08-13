---
title: VersionIndependentProgID
description: Ordnet eine ProgID einer CLSID zu. Dieser Wert wird verwendet, um die neueste Version einer Objektanwendung zu bestimmen.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe1defaa52df5251d6c021655d6e84c90677e2a2d57f0bfb67f925e0ffa5bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549716"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

Ordnet eine ProgID einer CLSID zu. Dieser Wert wird verwendet, um die neueste Version einer Objektanwendung zu bestimmen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert,** der die neueste Version der Objektanwendung angibt.

Die versionsunabhängige ProgID wird ausschließlich vom Anwendungscode gespeichert und verwaltet. Wenn die versionsunabhängige ProgID angegeben wird, gibt die [**CLSIDFromProgID-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) die CLSID der aktuellen Version zurück.

Sie können [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) und [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) verwenden, um zwischen diesen beiden Darstellungen zu konvertieren.

 

 




