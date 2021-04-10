---
title: Com+-Dienste werden veröffentlicht.
description: COM-basierte Dienste stellen einen Anwendungs Proxy in Form eines Windows Installer (MSI)-Pakets bereit.
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Com+-Dienste werden veröffentlicht.
- Active Directory, verwenden, Veröffentlichen eines Diensts, com+-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036348"
---
# <a name="publishing-com-services"></a>Com+-Dienste werden veröffentlicht.

COM-basierte Dienste stellen einen Anwendungs Proxy in Form eines Windows Installer (MSI)-Pakets bereit. Diese MSI-Datei enthält den zu verwendenden Servernamen und andere erforderliche Elemente, wie z. b. Proxy/Stub und Typbibliotheken, die für das Marshalling erforderlich sind. Das Snap-in "Komponenten Dienste" generiert automatisch diese Anwendungs Proxys für com+-Server Anwendungen.

Die Anwendungs Proxys werden in Active Directory mithilfe des Gruppenrichtlinie-Editors in-Richtlinien Objekten veröffentlicht. In der Client Anwendung ist kein spezieller Eingriff erforderlich. Das Computer-/Benutzerkonto auf dem Client Computer muss sich in einer OE befinden, die für die Verwendung des Richtlinien Objekts konfiguriert ist, in dem die Anwendungs Proxys veröffentlicht werden. Der com-Binder verwendet den Server automatisch mithilfe des Verzeichnisses, wenn der Client eine Instanz der betroffenen Objekte festlegt.

 

 




