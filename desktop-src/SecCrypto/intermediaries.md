---
description: Vermittler kommunizieren mit Clientanwendungen, damit sie Zertifikatanforderungen übermitteln können, und (vorausgesetzt, die Anforderung führt zu einem ausgestellten Zertifikat), um das ausgestellte Zertifikat auf den Client herunterzuladen.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: Zwischenstufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f9dbd48d5af575658c04760740ad0b1f64f373d76bb20ba80253b874c67de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005288"
---
# <a name="intermediaries"></a>Zwischenstufen

Vermittler kommunizieren mit Clientanwendungen, damit sie [*Zertifikatanforderungen*](../secgloss/c-gly.md)übermitteln und (vorausgesetzt, die Anforderung führt zu einem ausgestellten Zertifikat), um das ausgestellte Zertifikat auf den Client herunterzuladen. Jedes Transportschichtprotokoll erfordert einen eigenen Vermittler.

Microsoft-Zertifikatdienste werden mit einem Vermittler (den Webregistrierungsseiten) für HTTP versendet. Ein weiteres Beispiel für einen Vermittler ist das MICROSOFT Windows Certificates MMC-Snap-In (das das Aufrufen des Zertifikatanforderungs-Assistenten ermöglicht). Wenn andere Transportschichtprotokolle mit Zertifikatdiensten verwendet werden sollen, kann ein Entwickler einen Vermittler für jedes gewünschte Transportschichtprotokoll erstellen.

Vermittler kommunizieren mit Zertifikatdiensten über die [**schnittstellen ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) und [**ICertConfig,**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) die von der Server-Engine bereitgestellt werden. Die [**ICertRequest::Submit-Methode**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) wird [](../secgloss/c-gly.md)verwendet, um eine Zertifikatanforderung zu übermitteln, und [**ICertRequest::GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) wird verwendet, um das resultierende ausgestellte Zertifikat zu erhalten. Auf ähnliche Weise [**wird ICertConfig::GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) verwendet, um zu bestimmen, welche Zertifizierungsstelle für die Ausstellung des Zertifikats verwendet werden kann.

Ein Vermittler ist nicht sprachabhängig. Es kann sich um ein programm in C++, Visual Basic, Java, Skript oder eine andere Sprache schreiben.

Zusätzlich zum Sammeln von Daten vom Client zum Erstellen einer Zertifikatanforderung kann ein Vermittler Anforderungsattribute angeben. Anforderungen, die [](../secgloss/c-gly.md) an eine Zertifizierungsstelle gesendet werden, die das Unternehmensrichtlinienmodul ausgeführt, müssen den Typ des angeforderten Zertifikats angeben, indem sie entweder ein CertificateTemplate-Attribut oder eine Zertifikatvorlagenerweiterung in der Anforderung selbst angeben.

Beachten Sie, dass Entwickler (und Vermittler) während der Erstellung einer Zertifikatanforderung für die Beibehaltung der Geheimnisse des privaten Schlüssels verantwortlich sind. Nachdem ein privater Schlüssel kompromittiert wurde (seine Geheimnisse verloren), ist er nicht mehr von Nutzen.

Die Zertifikatdienste-Webregistrierungsseiten verwenden die Zertifikatregistrierungsschnittstellen, die private Schlüssel schützt, indem sie auf der Arbeitsstation generiert werden. [](cryptography-interfaces.md) Zusätzlich zur Beibehaltung der Geheimnisse des privaten Schlüssels ermöglicht das Zertifikatregistrierungssteuersystem einem Vermittler die Angabe des Kryptografiedienstanbieters, der Schlüsselspezifikation, der Schlüsselstärke und des Hashalgorithmus.

Das MMC-Snap-In Zertifikate verwendet auch die Zertifikatregistrierungssteuerung (Certificate Enrollment Control, Xenroll.dll). Wenn die Zertifikatdienste-Webregistrierungsseiten jedoch bewirken, dass die Ressource für die Zertifikatregistrierungssteuerung (Xenroll.dll) bei Bedarf auf den Client heruntergeladen wird, wird das MMC-Snap-In Zertifikate in einer Umgebung ausgeführt, in der Xenroll.dll bereits eine verfügbare Ressource ist.

Zusätzlich zu [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) und [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)finden Entwickler [](cryptography-interfaces.md) von Vermittlern möglicherweise die Schnittstellen für die Zertifikatregistrierung und das [Smartcard-Registrierungssteuersystem](certificate-enrollment-control.md) als nützlich.

 

 
