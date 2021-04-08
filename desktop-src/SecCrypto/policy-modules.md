---
description: Richtlinien Module sind Programme, die Anforderungen von den Zertifikat Diensten empfangen, diese Anforderungen auswerten und optionale Eigenschaften der Zertifikate angeben, die zum Ausfüllen dieser Anforderungen erstellt werden.
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: Richtlinien Module
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781a88ab714c402ea1670ac8c18ae4d80eb776e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960635"
---
# <a name="policy-modules"></a>Richtlinien Module

Richtlinien Module sind Programme, die Anforderungen von den Zertifikat Diensten empfangen, diese Anforderungen auswerten und optionale Eigenschaften der Zertifikate angeben, die zum Ausfüllen dieser Anforderungen erstellt werden. Ein Richtlinien Modul wird als [*Dynamic Link Library*](../secgloss/d-gly.md) (dll) implementiert. Ein Richtlinien Modul kann die [icertserverpolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) -Schnittstelle für die Kommunikation mit Zertifikat Diensten verwenden. Die Zertifikat Dienste kommunizieren mit einem Richtlinien Modul mithilfe von direkten com-aufrufen oder, wenn das Modul direkte com-Aufrufe nicht unterstützt, mithilfe von Automation.

Ein Richtlinien Modul kann vorhandene Zertifikat Eigenschaften und-Erweiterungen anzeigen, und es kann auch Anforderungs Attribute und-Eigenschaften anzeigen. Außerdem kann ein Richtlinien Modul Zertifikat Erweiterungen, die Eigenschaften "NotBefore" und "notAfter" sowie den [*relativen Distinguished Name*](../secgloss/r-gly.md) (RDN) eines Zertifikat Antragstellers festlegen oder ändern, abhängig von bestimmten Einschränkungen. Ein Richtlinien Modul gibt letztendlich die [*Zertifikat Anforderung*](../secgloss/c-gly.md) aus oder verweigert diese oder hält Sie an.

Vor dem Schreiben eines benutzerdefinierten Richtlinien Moduls sollten Sie die Verwendung eines der Standardrichtlinien Module in Erwägung gezogen. Sowohl die Zertifizierungsstelle der Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) der Zertifizierungsstelle als auch die eigenständige Zertifizierungsstelle werden mit einem entsprechenden Standardrichtlinien Modul ausgeliefert. Sowohl das Enterprise-als auch das eigenständige Standardrichtlinien Modul geben Zertifikat Anforderungen aus (die eigenständige Standard Richtlinie besteht jedoch darin, das Zertifikat zu speichern, bis es manuell von einem Administrator ausgestellt wird). Eine Unternehmens Zertifizierungsstelle sollte nur das von Microsoft bereitgestellte Enterprise Policy-Modul verwenden.

Die Unternehmens Zertifizierungsstelle erfordert Active Directory. Zu den zusätzlichen Features des Standardrichtlinien Moduls zählen Zertifikat Vorlagen, die [*Zugriffs Steuerungs Liste*](../secgloss/a-gly.md) (ACL) für die Zertifikat Vorlagen, um sicherzustellen, dass Anforderungen nur an autorisierte, vordefinierte Erweiterungen, die dem ausgestellten Zertifikat hinzugefügt werden, und Unterstützung für Smartcard-Domänen Anmelde Zertifikate ausgestellt werden.

Das standardmäßige eigenständige Zertifizierungsstellen-Richtlinien Modul unterstützt viele der Funktionen des standardmäßigen Enterprise-Moduls nicht, aber die Ausstellung von Smartcardzertifikaten wird unterstützt. Spezifische Details und die aktuellsten Funktionen des Standardrichtlinien Moduls finden Sie in der Produktdokumentation.

Bei Installationen, bei denen das Standardrichtlinien Modul nicht akzeptabel ist, können Zertifikat Dienste benutzerdefinierte Richtlinien Module zulassen. Weitere Informationen finden Sie unter [Schreiben von benutzerdefinierten Richtlinien Modulen](writing-custom-modules.md).

 

 
