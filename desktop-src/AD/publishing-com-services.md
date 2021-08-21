---
title: Veröffentlichen von COM+-Diensten
description: COM-basierte Dienste stellen einen Anwendungsproxy in Form eines MSI-Pakets (Windows Installer) zur Verfügung.
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Veröffentlichen von COM+-Diensten
- Active Directory, Verwenden, Veröffentlichen eines Diensts, COM+-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91801bbfcbf8efa34ac0b79477dd9d859fc2ed34a8d40bcf0bd829f82cfd571a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025428"
---
# <a name="publishing-com-services"></a>Veröffentlichen von COM+-Diensten

COM-basierte Dienste stellen einen Anwendungsproxy in Form eines MSI-Pakets (Windows Installer) zur Verfügung. Diese .msi datei enthält den zu verwendenden Servernamen und andere erforderliche Elemente, z. B. Proxy/Stubs und Typbibliotheken, die für das Marshalling erforderlich sind. Das Komponentendienste-Snap-In generiert diese Anwendungsproxies automatisch für COM+-Serveranwendungen.

Die Anwendungsproxies werden in Richtlinienobjekten in Active Directory mithilfe des Gruppenrichtlinie veröffentlicht. In der Clientanwendung ist kein spezieller Eingriff erforderlich. Der Computer/das Benutzerkonto auf dem Clientcomputer muss sich in einer Organisationseinheit befinden, die für die Verwendung des Richtlinienobjekts konfiguriert ist, in dem die Anwendungsproxies veröffentlicht werden. Der COM-Binder sucht den Server automatisch über das Verzeichnis, wenn der Client eine Instanz der betreffenden Objekte ein richtet.

 

 




