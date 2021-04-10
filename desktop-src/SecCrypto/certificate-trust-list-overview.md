---
description: Zusätzlich zu den Zertifikaten und Zertifikat Sperr Listen (CRL) unterstützt der kryptoapi-Zertifikat Speicher die Zertifikats Vertrauens Liste (Certificate Trust List, CTL).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Übersicht über Zertifikat Vertrauens Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bdbd8b5fdfe4b2d81f3faddb052c16ecf32428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867196"
---
# <a name="certificate-trust-list-overview"></a>Übersicht über Zertifikat Vertrauens Listen

Zusätzlich zu den Zertifikaten und [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRL) unterstützt [*der kryptoapi*](../secgloss/c-gly.md) - [*Zertifikat Speicher*](../secgloss/c-gly.md) die [*Zertifikats Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL). Eine CTL ist eine vordefinierte Liste von Elementen, die von einer vertrauenswürdigen Entität signiert wurden. Eine CTL ist eine Liste von Zertifikaten oder eine [*Liste mit Datei*](../secgloss/h-gly.md) Namen. Alle Elemente in der Liste werden von einer vertrauenswürdigen Signatur Entität authentifiziert und genehmigt. Eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur ähnelt den Kontext Strukturen Certificate und CRL. Ein CTL-Kontext kann im Zertifikat Speicher persistent gespeichert werden.

Eine kryptoapi-CTL ist eine Liste von Elementen, die von einer vertrauenswürdigen Entität signiert wurden. Die Liste der Elemente kann etwas sein, z. b. eine Liste mit Hashes von Zertifikaten oder eine Liste mit Dateinamen. In den meisten Fällen ist eine CTL eine Liste mit Hash Zertifikat Kontexten. Alle Elemente in der Liste werden von der Signatur Entität authentifiziert und genehmigt. Die primäre Verwendung von CTLs ist die Überprüfung signierter Nachrichten mithilfe der CTL als Quelle vertrauenswürdiger Stamm [*Zertifikate*](../secgloss/r-gly.md).

Die [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur ähnelt den Kontext Strukturen Certificate und CRL, aber im Gegensatz zu den Kontext Strukturen Certificate und CRL enthält die **CTL- \_ Kontext** Struktur einen **hcryptmsg** -Member. Dieses Handle wird durch einen-Vorgang geöffnet, der eine **CTL- \_ Kontext** Struktur zurückgibt, sodass die Nachrichten Funktionen verwendet werden können, um die Signatur der CTL zu überprüfen. Diese Überprüfung ist erforderlich, um sicherzustellen, dass eine CTL keine falsche CTL ist, die von einer nicht autorisierten Entität gepflanzt wird.

Verfahren zum Erstellen einer signierten CTL und zum Speichern in einem Zertifikat Speicher finden Sie unter [erstellen, Signieren und Speichern einer CTL](creating-signing-and-storing-a-ctl.md). Weitere Informationen finden Sie unter über [Prüfen einer CTL](verifying-a-ctl.md) und über [Prüfen von signierten Nachrichten mithilfe von CTLs](verifying-signed-messages-by-using-ctls.md) .

 

 
