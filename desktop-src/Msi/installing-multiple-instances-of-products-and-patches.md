---
description: 'Windows Das Installationsprogramm ermöglicht die Installation einer Instanz eines Produktcodes pro Kontext, und die beiden möglichen Kontexttypen sind: MachineUser Wenn ein Produktcode unverändert bleibt, kann nur eine Instanz im Computerkontext installiert werden, und nur eine Instanz kann in jedem Benutzerkontext installiert werden. Damit mehrere Instanzen isoliert bleiben, müssen sie unterschiedliche Produktcodes aufweisen und können keine Dateidaten oder Nichtdateidaten freigeben. Der Windows Installer kann nicht mehrere Instanzen von Produkten mit gleichzeitigen Installationen installieren. Sie können jedoch mehrere Instanzen eines Produkts installieren, wenn Sie über ein separates Installationspaket für jede Instanz eines Produkts oder Patches verfügen. Anschließend kann jedes Paket einen eigenen Satz von Daten behalten und über einen eigenen eindeutigen Produktcode verfügen. Ab dem Installationsprogramm, das Windows Server 2003 und Windows XP mit Service Pack 1 (SP1) ausführt, können Sie mehrere Instanzen eines Produkts mithilfe von Produktcodetransformationen und einem .msi Paket oder einem Patch installieren. Sie können auch Codetransformationen verwenden, um mehrere Instanzen eines Produkts mit Windows 2000 mit Service Pack 4 (SP4) und Windows Installer&\# 160 zu installieren. 3.0. Die einzige Möglichkeit, mehrere Instanzen eines Produkts mit früheren Versionen des Installationsprogramms zu installieren, besteht darin, für jede Instanz ein separates Installationspaket zu verwenden. Die Verwendung von Instanztransformationen reduziert den Aufwand, der erforderlich ist, um mehrere Instanzen eines Produkts zu unterstützen. Sie können eine Basis Windows Installer-Pakets für ein Produkt und dann mehrere Instanztransformationen erstellen, die den Produktcode ändern und Daten für jede Instanz verwalten. Weitere Informationen finden Sie unter Erstellen mehrerer Instanzen mit Instanztransformationen und Installieren mehrerer Instanzen mit Instanztransformationen.'
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Installieren mehrerer Instanzen von Produkten und Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c9f061ef203effc4ec71c386f17a4c92bae957610fdc3a15b0c64a92e1e024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946148"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Installieren mehrerer Instanzen von Produkten und Patches

Windows Das Installationsprogramm ermöglicht die Installation einer Instanz eines Produktcodes pro Kontext, und die beiden möglichen Kontexttypen lauten wie folgt:

-   Machine
-   Benutzer

Wenn ein Produktcode unverändert bleibt, kann nur eine Instanz im Computerkontext und nur eine Instanz in jedem Benutzerkontext installiert werden.

Damit mehrere Instanzen isoliert bleiben, müssen sie unterschiedliche Produktcodes aufweisen und können keine Dateidaten oder Nichtdateidaten freigeben. Der Windows Installer kann nicht mehrere Instanzen von Produkten mit [gleichzeitigen Installationen](concurrent-installations.md)installieren. Sie können jedoch mehrere Instanzen eines Produkts installieren, wenn Sie über ein separates Installationspaket für jede Instanz eines Produkts oder Patches verfügen. Anschließend kann jedes Paket einen eigenen Satz von Daten behalten und über einen eigenen eindeutigen Produktcode verfügen.

Ab dem Installationsprogramm, das Windows Server 2003 und Windows XP mit Service Pack 1 (SP1) ausführt, können Sie mehrere Instanzen eines Produkts mithilfe von Produktcodetransformationen und einem .msi Paket oder einem Patch installieren. Sie können auch Codetransformationen verwenden, um mehrere Instanzen eines Produkts mit Windows 2000 mit Service Pack 4 (SP4) und Windows Installer 3.0 zu installieren. Die einzige Möglichkeit, mehrere Instanzen eines Produkts mit früheren Versionen des Installationsprogramms zu installieren, besteht darin, für jede Instanz ein separates Installationspaket zu verwenden.

Die Verwendung von Instanztransformationen reduziert den Aufwand, der erforderlich ist, um mehrere Instanzen eines Produkts zu unterstützen. Sie können ein Basis-Windows Installer-Paket für ein Produkt und dann mehrere Instanztransformationen erstellen, die den Produktcode ändern und Daten für jede Instanz verwalten.

Weitere Informationen finden Sie unter [Erstellen mehrerer Instanzen mit Instanztransformationen](authoring-multiple-instances-with-instance-transforms.md) und Installieren mehrerer Instanzen mit [Instanztransformationen.](installing-multiple-instances-with-instance-transforms.md)

 

 



