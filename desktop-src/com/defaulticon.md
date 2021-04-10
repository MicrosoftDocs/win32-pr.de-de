---
title: DefaultIcon
description: Stellt Standard Symbol Informationen für die ikonischen Präsentationen von Objekten bereit.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039661"
---
# <a name="defaulticon"></a>DefaultIcon

Stellt Standard Symbol Informationen für die ikonischen Präsentationen von Objekten bereit.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der den vollständigen Pfad zum Namen der Objekt Anwendung und den Ressourcen Index des Symbols in der ausführbaren Datei angibt.

**DefaultIcon** identifiziert das Symbol, das verwendet werden soll, wenn beispielsweise ein-Steuerelement auf ein Symbol minimiert wird. Dieser Eintrag enthält den vollständigen Pfad des ausführbaren namens der Serveranwendung und den Ressourcen Index des Symbols in der ausführbaren Datei. Anwendungen können die von **DefaultIcon** bereitgestellten Informationen verwenden, um ein Symbol Handle mit [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona)abzurufen.

 

 