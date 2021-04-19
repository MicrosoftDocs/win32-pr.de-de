---
description: Das Microsoft .NET Framework bietet Ihnen die Möglichkeit, Anwendungen von einem Web-oder Dateiserver bereitzustellen.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Keine Berührungs Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6567edf35dbd79256bed228de3941351bd5e7642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361751"
---
# <a name="no-touch-deployment"></a>Keine Berührungs Bereitstellung

Das Microsoft .NET Framework bietet Ihnen die Möglichkeit, Anwendungen von einem Web-oder Dateiserver bereitzustellen. Diese Technik, die als "No-Berührungs-Bereitstellung" bezeichnet wird, kombiniert die Leistung und Interaktivität einer intelligenten Client Anwendung mit allen Vorteilen der Bereitstellung einer Webanwendung. Zum Bereitstellen der Anwendung über das Web klicken Sie mit der rechten Maustaste auf den Ordner mit der ausführbaren Datei, und wählen Sie **Eigenschaften** aus. Wählen Sie auf der Registerkarte **Webfreigabe** die Option **diesen Ordner freigeben** aus. Geben Sie einen Alias für den Ordner ein. Nun können Sie die ausführbare Datei über das Internet ausführen, indem Sie diesen Alias als Verzeichnis auf dem Server verwenden. Weitere Informationen zur Bereitstellung ohne Fingereingabe finden Sie unter [.net Intelligent Clients](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) und [No-Touchscreen Deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> Sie müssen Microsoft Internetinformationsdienste (IIS) auf Ihrem Computer installiert haben, um die Registerkarte **Webfreigabe** im Dialogfeld **Eigenschaften** zu aktivieren.

 

Die Bereitstellung ohne Fingereingabe wird auf die auf Freihand aktivierte Anwendungen auf die gleiche Weise wie jede andere Windows Forms Anwendung angewendet. Die vom Microsoft Windows XP Tablet PC Edition-SDK (Software Development Kit) bereitgestellten Beispiele beinhalten eine nicht Berührungs bezogene Bereitstellungs Version des Beispiels "Automatische Ansprüche" im Abschnitt "Ink Web Samples" der Beispiele. In diesem Beispiel wird das ursprüngliche [Formular Beispiel für automatische Ansprüche](auto-claims-form-sample.md) übernommen und ein Installationsprogramm bereitstellt, das eine Webfreigabe vornimmt. Wenn Microsoft Internet Explorer zu AutoClaims.exe im Verzeichnis navigiert, das der Webfreigabe zugeordnet ist, wird die Anwendung gestartet. Weitere Informationen zu diesem Beispiel finden Sie unter Beispiel für die [Bereitstellung ohne Benutzer](no-touch-deployment-web-sample.md) Eingriff.

> [!Note]  
> Wenn Sie eine .NET-Anwendung über das Internet bereitstellen, kann die Anwendung vom .net-Sicherheitsmodell betroffen sein. Im Abschnitt " [Sicherheit und Vertrauens](security-and-trust.md) Stellung" wird beschrieben, wie die Sicherheit mit frei Hand fähigen Webanwendungen funktioniert.

 

 

 