---
title: ADSI-Erweiterungstypbibliotheken
description: Die Typbibliotheken für Erweiterungen werden nicht zusammengeführt.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI-Erweiterungstypbibliotheken ADSI
- Extensions ADSI , Erweiterungstypbibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2390f587d5ce0d18e6e96aaf993115bb523feb340bf2becf60ceb2cff81d952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180830"
---
# <a name="adsi-extension-type-libraries"></a>ADSI-Erweiterungstypbibliotheken

Die Typbibliotheken für Erweiterungen werden nicht zusammengeführt. ADSI-Clients müssen speziell die Typbibliothek für jede Erweiterung enthalten. Die Typbibliothek ist erforderlich, damit Visual Basic Bindungen aktivieren können. In C/C++ geschriebene Clientanwendungen können die **QueryInterface-Methode** für die Erweiterungsschnittstellen aufrufen, die in den Erweiterungsheaderdateien definiert sind.

 

 




