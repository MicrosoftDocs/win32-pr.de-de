---
description: Die Microsoft .NET Framework bietet Ihnen die Möglichkeit, Anwendungen über einen Web- oder Dateiserver bereitzustellen.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Keine Touchbereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d31f01742a1b1231171688ea15634913c56ef613c8f6ebdaf3042b4998f00a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856539"
---
# <a name="no-touch-deployment"></a>Keine Touchbereitstellung

Die Microsoft .NET Framework bietet Ihnen die Möglichkeit, Anwendungen über einen Web- oder Dateiserver bereitzustellen. Diese Technik, die als "No-Touch-Bereitstellung" bezeichnet wird, kombiniert die Leistung und Interaktivität einer intelligenten Clientanwendung mit allen Bereitstellungsvorteilen einer Webanwendung. Um Ihre Anwendung über das Web bereitzustellen, klicken Sie mit der rechten Maustaste auf den Ordner, der Die ausführbare Datei enthält, und wählen Sie **Eigenschaften** aus. Wählen Sie auf der Registerkarte **Webfreigabe** die Option **Diesen Ordner freigeben** aus. Geben Sie einen Alias für den Ordner ein. Jetzt kann Ihre ausführbare Datei über das Web ausgeführt werden, indem Sie diesen Alias als Verzeichnis auf Ihrem Server verwenden. Weitere Informationen zur Bereitstellung ohne Toucheingabe finden Sie unter [.NET Smart Clients](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) und [No-Touch Deployment im .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> Sie müssen Microsoft-Internetinformationsdienste (IIS) auf Ihrem Computer installiert haben, um die Registerkarte **Webfreigabe** im Dialogfeld **Eigenschaften** zu aktivieren.

 

Die Bereitstellung ohne Toucheingabe wird auf die gleiche Weise wie jede andere Windows Forms-Anwendung auf Freihandanwendungen angewendet. Die vom Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) bereitgestellten Beispiele enthalten eine bereitstellungsfreie Version des Beispiels für automatische Ansprüche im Abschnitt Ink-Webbeispiele der Beispiele. Dieses Beispiel verwendet das ursprüngliche [Formularbeispiel](auto-claims-form-sample.md) für automatische Ansprüche und stellt ein Installationsprogramm bereit, das eine Webfreigabe eingibt. Wenn Microsoft Internet Explorer zu AutoClaims.exe im Verzeichnis navigiert, das der Webfreigabe zugeordnet ist, wird die Anwendung gestartet. Weitere Informationen zum Beispiel finden Sie unter [Webbeispiel](no-touch-deployment-web-sample.md) für die Bereitstellung ohne Toucheingabe.

> [!Note]  
> Wenn Sie eine .NET-Anwendung über das Web bereitstellen, ist die Anwendung möglicherweise vom .NET-Sicherheitsmodell betroffen. Im Abschnitt [Sicherheit und Vertrauensstellung](security-and-trust.md) wird die Funktionsweise der Sicherheit mit Ink-fähigen Webanwendungen beschrieben.

 

 

 