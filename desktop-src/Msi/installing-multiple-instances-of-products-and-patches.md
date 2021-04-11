---
description: 'Windows Installer ermöglicht, dass eine Instanz eines Produktcodes pro Kontext installiert werden kann. die beiden möglichen Kontext Typen lauten wie folgt: machineuser wenn ein Produktcode unverändert bleibt, kann nur eine Instanz im Computer Kontext installiert werden, und es kann nur eine Instanz in jedem Benutzer Kontext installiert werden. Damit mehrere Instanzen isoliert bleiben, müssen Sie über unterschiedliche Produktcodes verfügen und keine Datei Daten oder nicht-Datei Daten freigeben. Der Windows Installer kann nicht mehrere Instanzen von Produkten mithilfe gleichzeitiger Installationen installieren. Sie können jedoch mehrere Instanzen eines Produkts installieren, wenn Sie über ein separates Installationspaket für jede Instanz eines Produkts oder Patches verfügen. Dann kann jedes Paket einen eigenen Satz von Daten behalten und einen eigenen eindeutigen Produktcode aufweisen. Ab dem Installer, auf dem Windows Server 2003 und Windows XP mit Service Pack 1 (SP1) ausgeführt wird, können Sie mehrere Instanzen eines Produkts mithilfe von Produktcode Transformationen und einem MSI-Paket oder einem Patch installieren. Mithilfe von Produktcode Transformationen können Sie auch mehrere Instanzen eines Produkts mit Windows 2000 mit Service Pack 4 (SP4) und Windows Installer&160 installieren \# . 3,0. Die einzige Möglichkeit, mehr als eine Instanz eines Produkts mit früheren Versionen des Installers zu installieren, besteht darin, ein separates Installationspaket für jede Instanz zu installieren. Durch die Verwendung von instanztransformationen wird der Aufwand für die Unterstützung mehrerer Instanzen eines Produkts erheblich reduziert. Sie können ein Basis Windows Installer Paket für ein Produkt und dann mehrere instanztransformationen erstellen, die den Produktcode ändern und die Daten für die einzelnen Instanzen verwalten. Weitere Informationen finden Sie unter Erstellen mehrerer Instanzen mit instanztransformationen und Installieren mehrerer Instanzen mit instanztransformationen.'
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Installieren mehrerer Instanzen von Produkten und Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3a1de5de7cc63d5eed2e191d77915630761561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218005"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Installieren mehrerer Instanzen von Produkten und Patches

Windows Installer ermöglicht die Installation einer Instanz eines Produktcodes pro Kontext, und die beiden möglichen Kontext Typen lauten wie folgt:

-   Machine
-   Benutzer

Wenn ein Produktcode unverändert bleibt, kann nur eine Instanz im Computer Kontext installiert werden, und es kann nur eine Instanz in jedem Benutzer Kontext installiert werden.

Damit mehrere Instanzen isoliert bleiben, müssen Sie über unterschiedliche Produktcodes verfügen und keine Datei Daten oder nicht-Datei Daten freigeben. Der Windows Installer kann nicht mehrere Instanzen von Produkten mithilfe [gleichzeitiger Installationen](concurrent-installations.md)installieren. Sie können jedoch mehrere Instanzen eines Produkts installieren, wenn Sie über ein separates Installationspaket für jede Instanz eines Produkts oder Patches verfügen. Dann kann jedes Paket einen eigenen Satz von Daten behalten und einen eigenen eindeutigen Produktcode aufweisen.

Ab dem Installer, auf dem Windows Server 2003 und Windows XP mit Service Pack 1 (SP1) ausgeführt wird, können Sie mehrere Instanzen eines Produkts mithilfe von Produktcode Transformationen und einem MSI-Paket oder einem Patch installieren. Sie können auch Produktcode Transformationen verwenden, um mehrere Instanzen eines Produkts mit Windows 2000 mit Service Pack 4 (SP4) und Windows Installer 3,0 zu installieren. Die einzige Möglichkeit, mehr als eine Instanz eines Produkts mit früheren Versionen des Installers zu installieren, besteht darin, ein separates Installationspaket für jede Instanz zu installieren.

Durch die Verwendung von instanztransformationen wird der Aufwand für die Unterstützung mehrerer Instanzen eines Produkts erheblich reduziert. Sie können ein Basis Windows Installer Paket für ein Produkt und dann mehrere instanztransformationen erstellen, die den Produktcode ändern und die Daten für die einzelnen Instanzen verwalten.

Weitere Informationen finden Sie unter [Erstellen mehrerer Instanzen mit instanztransformationen](authoring-multiple-instances-with-instance-transforms.md) und [Installieren mehrerer Instanzen mit instanztransformationen](installing-multiple-instances-with-instance-transforms.md).

 

 



