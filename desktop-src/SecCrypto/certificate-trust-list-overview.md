---
description: Zusätzlich zu Zertifikaten und Zertifikatsperrlisten (Certificate Revocation Lists, CRL) unterstützt der CryptoAPI-Zertifikatspeicher die Zertifikatvertrauensliste (Certificate Trust List, CTL).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Übersicht über die Zertifikatvertrauensliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7906f02e9af3534445c5b1d6a48c94653feb78b57c71a23acfd9af51477cd050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771106"
---
# <a name="certificate-trust-list-overview"></a>Übersicht über die Zertifikatvertrauensliste

Zusätzlich zu Zertifikaten und [*Zertifikatsperrlisten*](../secgloss/c-gly.md) (Certificate Revocation Lists, CRL) unterstützt der [*CryptoAPI-Zertifikatspeicher*](../secgloss/c-gly.md) [](../secgloss/c-gly.md) die [*Zertifikatvertrauensliste*](../secgloss/c-gly.md) (Certificate Trust List, CTL). Eine CTL ist eine vordefinierte Liste von Elementen, die von einer vertrauenswürdigen Entität signiert wurden. Eine CTL ist eine Liste von Hashes von [*Zertifikaten*](../secgloss/h-gly.md) oder eine Liste von Dateinamen. Alle Elemente in der Liste werden von einer vertrauenswürdigen Signaturentität authentifiziert und genehmigt. Eine [**CTL \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) ähnelt Zertifikat- und Zertifikatsperrlisten-Kontextstrukturen. Ein CTL-Kontext kann im Zertifikatspeicher beibehalten werden.

Eine CryptoAPI-CTL ist eine Liste von Elementen, die von einer vertrauenswürdigen Entität signiert wurden. Die Liste der Elemente kann beliebig sein, z. B. eine Liste von Hashes von Zertifikaten oder eine Liste von Dateinamen. In den meisten Fällen ist eine CTL eine Liste von Hashzertifikatkontexten. Alle Elemente in der Liste werden von der Signaturentität authentifiziert und genehmigt. Die primäre Verwendung von CTLs besteht darin, signierte Nachrichten zu überprüfen, wobei die CTL als Quelle für vertrauenswürdige [*Stammzertifikate*](../secgloss/r-gly.md)verwendet wird.

Die [**CTL \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) ähnelt den Zertifikat- und Zertifikatsperrlisten-Kontextstrukturen. Im Gegensatz zu den Zertifikat- und CRL-Kontextstrukturen enthält die **CTL \_ CONTEXT-Struktur** jedoch einen **hCryptMsg-Member.** Dieses Handle wird durch einen Aufruf einer der Funktionen geöffnet, die eine **CTL \_ CONTEXT-Struktur** zurückgeben, sodass die Nachrichtenfunktionen verwendet werden können, um die Signatur der CTL zu überprüfen. Diese Überprüfung ist erforderlich, um sicherzustellen, dass eine CTL keine gefälschte CTL ist, die von einer nicht autorisierten Entität plant wird.

Verfahren zum Erstellen einer signierten CTL und speichern sie in einem Zertifikatspeicher finden Sie unter [Erstellen, Signieren und Speichern einer](creating-signing-and-storing-a-ctl.md)Zertifikatsgültigkeitsdauer. Unter [Verifying a CTL (Überprüfen einer CTL)](verifying-a-ctl.md) und [Verifying Signed Messages By Using CTLs (Überprüfen von signierten Nachrichten mithilfe von CTLs)](verifying-signed-messages-by-using-ctls.md) finden Sie auch Schritt-für-Schritt-Überprüfungsverfahren.

 

 
