---
description: Vermittler kommunizieren mit Client Anwendungen, um Ihnen das Übermitteln von Zertifikat Anforderungen zu ermöglichen, und (vorausgesetzt, dass die Anforderung ein ausgestelltes Zertifikat ergibt), um das ausgegebene Zertifikat auf den Client herunterzuladen.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: Zwischenstufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 040e79abb03bd0363d37fdad79f7311412b0ffe2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364281"
---
# <a name="intermediaries"></a>Zwischenstufen

Vermittler kommunizieren mit Client Anwendungen, um Ihnen das Übermitteln von [*Zertifikat Anforderungen*](../secgloss/c-gly.md)zu ermöglichen, und (vorausgesetzt, dass die Anforderung ein ausgestelltes Zertifikat ergibt), um das ausgegebene Zertifikat auf den Client herunterzuladen. Jedes Transportschicht Protokoll erfordert einen eigenen Vermittler.

Die Microsoft-Zertifikat Dienste werden mit einem Vermittler (den Webregistrierungs Seiten) für http ausgeliefert. Ein weiteres Beispiel für einen Vermittler ist das Microsoft Windows-Zertifikate-MMC-Snap-in (das den Aufruf des Zertifikatanforderungs-Assistenten ermöglicht). Wenn andere Transportschicht Protokolle mit Zertifikat Diensten verwendet werden sollen, kann ein Entwickler einen Vermittler für jedes gewünschte Transportschicht Protokoll erstellen.

Vermittler kommunizieren mithilfe der [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) -und [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) -Schnittstellen, die von der Server-Engine bereitgestellt werden, mit Zertifikat Diensten. Die [**ICertRequest:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) -Methode wird verwendet, um eine [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu senden, und [**ICertRequest:: GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) wird verwendet, um das resultierende ausgegebene Zertifikat zu erhalten. Entsprechend wird [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) verwendet, um zu bestimmen, welche Zertifizierungsstelle zum Ausstellen des Zertifikats verwendet werden kann.

Ein Vermittler ist nicht sprachabhängig. Dabei kann es sich um ein Programm handeln, das in C++, Visual Basic, Java, Script oder einer anderen Sprache geschrieben ist.

Zusätzlich zum Sammeln von Daten vom Client zum Erstellen einer Zertifikat Anforderung kann ein Vermittler Anforderungs Attribute angeben. Anforderungen an eine [*Zertifizierungs*](../secgloss/c-gly.md) Stelle, die das Enterprise-Richtlinien Modul ausführen, müssen den Typ des angeforderten Zertifikats angeben, indem Sie in der Anforderung entweder ein "certificatetemplate"-Attribut oder eine Zertifikat Vorlagen Erweiterung angeben.

Beachten Sie, dass Entwickler (und Vermittler) während der Erstellung einer Zertifikat Anforderung dafür verantwortlich sind, das Geheimnis des privaten Schlüssels aufrechtzuerhalten. Wenn ein privater Schlüssel kompromittiert wurde (seine Geheimhaltung verliert), ist er nutzlos.

Die Webregistrierungs-Seiten der Zertifikat Dienste verwenden die [Zertifikat Registrierungs Schnittstellen](cryptography-interfaces.md), die private Schlüssel schützen, indem Sie auf der Arbeitsstation erstellt werden. Zusätzlich zur Aufrechterhaltung des Geheimnisses des privaten Schlüssels ermöglicht die Zertifikat Registrierungs Steuerung einem Vermittler, den Kryptografiedienstanbieter, die Schlüssel Spezifikation, die Schlüssel Stärke und den Hash Algorithmus anzugeben.

Das MMC-Snap-in "Zertifikate" verwendet auch das Zertifikat Registrierungs Steuerelement (Xenroll.dll). Wenn die Webregistrierungs Seiten der Zertifikat Dienste jedoch bewirken, dass die Zertifikatregistrierungs-Steuerungs Ressource (Xenroll.dll) bei Bedarf auf den Client heruntergeladen wird, wird das MMC-Snap-in "Zertifikate" in einer Umgebung ausgeführt, in der Xenroll.dll bereits eine verfügbare Ressource ist.

Zusätzlich zu [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) und [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)finden Entwickler von Vermittler möglicherweise die [Zertifikat Registrierungs Schnittstellen](cryptography-interfaces.md) und die [Smartcard](certificate-enrollment-control.md) -Registrierungs Steuerung als nützlich.

 

 
