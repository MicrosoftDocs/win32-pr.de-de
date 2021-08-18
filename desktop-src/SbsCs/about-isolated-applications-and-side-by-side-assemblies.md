---
description: Isolierte Anwendungen und side-by-side-Assemblys bieten eine Lösung, die Konflikte bei der DLL-Versionierung reduziert. Sie ermöglichen Anwendungen das sichere Freigeben von Assemblys. Weitere Informationen finden Sie unter Freigegebene Assemblys.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Informationen zu isolierten Anwendungen und nebenseitigen Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ab72689173d4e8942d10dfc62259091574634227c3f4d252b0d87853ec9be7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142663"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Informationen zu isolierten Anwendungen und nebenseitigen Assemblys

[Isolierte Anwendungen](isolated-applications.md) und [side-by-side-Assemblys](about-side-by-side-assemblies-.md) bieten eine Lösung, die Konflikte bei [*der DLL-Versionierung reduziert.*](d-sbscs-gly.md) Sie ermöglichen Anwendungen das sichere Freigeben von Assemblys. Weitere Informationen finden Sie unter [Freigegebene Assemblys.](/windows/desktop/Msi/shared-assemblies)

Eine Assembly ist eine grundlegende Einheit für das Benennen, Binden, Versionieren, Bereitstellen oder Konfigurieren eines Blocks von Programmiercode. Anwendungen mit gemeinsamer Funktionalität können freigegebene Codeblöcke ausführen, die als Module oder Codeassemblys bezeichnet werden. Diese Codeassemblys können in DLLs oder COM-Assemblys platziert werden. Die Infrastruktur für die sichere Freigabe von Assemblys wird als gemeinsame Assemblyfreigabe bezeichnet.

[Bei gleichzeitigen Assemblys](about-side-by-side-assemblies-.md) handelt es sich um Codeassemblys, die von Manifesten beschrieben und so verfasst werden, dass mehrere Versionen gleichzeitig ausgeführt werden können, ohne dass ein Konflikt miteinander in Konflikt stehen muss. [](manifests.md) Wenn Entwickler Manifeste erstellen und Anwendungen schreiben, um die gleichzeitige Assemblyfreigabe zu [verwenden,](side-by-side-assembly-sharing.md)können mehrere Assemblyversionen auf dem System ausgeführt werden, und jede Anwendung kann angeben, welche Assemblyversion sie verwenden soll.

Eine typische [*nebenseitige Assembly ist*](s-sbscs-gly.md) eine einzelne DLL mit einem einzelnen Manifest. Bei assemblyseitigen Assemblys werden die Informationen zur Bindung und COM-Aktivierung, die üblicherweise in der Registrierung gespeichert werden, in Manifesten gespeichert. In einigen Fällen können die in Manifesten angegebenen Versionen der Assembly auf globaler oder anwendungsspezifischer Basis von Assemblyherausgebern, Anwendungsentwicklern oder Administratoren geändert werden. Weitere Informationen finden Sie unter [Standardkonfiguration,](default-configuration.md) [Herausgeberkonfiguration](publisher-configuration.md)und [anwendungsspezifische Konfiguration.](per-application-configuration.md)

Entwickler können die von Microsoft oder anderen Herausgebern von nebeneinander bereitgestellten Assemblys in ihren Anwendungen verwenden. Entwickler können z. B. die Funktionalität der aktualisierten allgemeinen Steuerelemente nutzen, z. B. das Design, indem sie ihre Anwendungen so entwerfen, dass sie die seiteseitige Assembly verwenden, die Comctl32.dll 6.0 enthält. Eine Liste der nebeneinander verfügbaren Assemblys und Manifeste, die mit Windows XP enthalten sind, finden Sie unter [Unterstützte microsoft-nebenseitige Assemblys.](supported-microsoft-side-by-side-assemblies.md) Entwickler können auch eigene, nebeneinander seitige Assemblys erstellen. Weitere Informationen finden Sie unter [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).

 

 
