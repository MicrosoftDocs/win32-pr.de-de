---
description: Isolierte Anwendungen und parallele Assemblys stellen eine Lösung bereit, die dll-Versions Verwaltungs Konflikte verringert. Sie ermöglichen es Anwendungen, Assemblys sicher freizugeben. Weitere Informationen finden Sie unter Freigegebene Assemblys.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Informationen zu isolierten Anwendungen und parallelen Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9099ca2e41d61c84e2952661b33ca008651f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131609"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Informationen zu isolierten Anwendungen und parallelen Assemblys

[Isolierte Anwendungen](isolated-applications.md) und [parallele](about-side-by-side-assemblies-.md) Assemblys stellen eine Lösung bereit, die [*dll-Versions Verwaltungs Konflikte*](d-sbscs-gly.md)verringert. Sie ermöglichen es Anwendungen, Assemblys sicher freizugeben. Weitere Informationen finden Sie unter frei [gegebene](/windows/desktop/Msi/shared-assemblies)Assemblys.

Eine Assembly ist eine grundlegende Einheit für das benennen, binden, Versionieren, bereitstellen oder Konfigurieren eines Blocks von Programmiercode. Anwendungen mit allgemeiner Funktionalität können freigegebene Blöcke von Programmiercode ausführen, die als Module oder Codeassemblys bezeichnet werden. Diese Codeassemblys können in DLLs oder COM-Assemblys abgelegt werden. Die Infrastruktur für die sichere Freigabe von Assemblys wird als parallele assemblyfreigabe bezeichnet.

Parallele Assemblys sind Codeassemblys [, die von](about-side-by-side-assemblies-.md) [Manifests](manifests.md) beschrieben und erstellt werden, sodass mehrere Versionen gleichzeitig ausgeführt werden können, ohne dass Konflikte miteinander in Konflikt stehen. Wenn Entwickler Manifeste verfassen und Anwendungen schreiben, [](side-by-side-assembly-sharing.md)um die parallele assemblyfreigabe zu verwenden, können mehrere Assemblyversionen auf dem System ausgeführt werden, und jede Anwendung kann angeben, welche Assemblyversion Sie verwenden soll.

Eine typische parallele [*Assembly*](s-sbscs-gly.md) ist eine einzelne DLL mit einem einzelnen Manifest. Parallele Assemblys speichern die Informationen über die Bindung und die COM-Aktivierung, die normalerweise in der Registrierung gespeichert sind, in Manifesten. In einigen Fällen können die in Manifeste angegebenen Versionen der Assembly auf globaler oder Anwendungs Basis von assemblyverlegern, Anwendungsentwicklern oder Administratoren geändert werden. Weitere Informationen finden Sie unter [Standardkonfiguration](default-configuration.md), [Verleger Konfiguration](publisher-configuration.md)und [Konfiguration pro Anwendung](per-application-configuration.md).

Entwickler können die parallelen Assemblys verwenden, die von Microsoft oder anderen parallelen assemblyverlegern in Ihren Anwendungen bereitgestellt werden. Entwickler können z. b. die Funktionalität der aktualisierten allgemeinen Steuerelemente, wie z. b. Design, nutzen, indem Sie Ihre Anwendungen so entwerfen, dass Sie die parallele Assembly verwenden, die Comctl32.dll 6,0 enthält. Eine Liste der parallelen Assemblys und Manifeste, die mit Windows XP ausgeliefert werden, finden Sie [unter Unterstützte](supported-microsoft-side-by-side-assemblies.md)parallele Assemblys von Microsoft. Entwickler können auch Ihre eigenen parallelen Assemblys erstellen. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md)paralleler Assemblys.

 

 
