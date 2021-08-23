---
description: Die Microsoft Digest wird durch den ersten Aufruf der AcceptSecurityContext-Funktion (Digest) des Servers generiert.
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Generieren der Digest-Herausforderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a01a7edfa6498ed621e351c114e65a6d4ff6ef7a75b459cb29e00f0dc668a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623330"
---
# <a name="generating-the-digest-challenge"></a>Generieren der Digest-Herausforderung

Die Microsoft Digest wird durch den ersten Aufruf der [**AcceptSecurityContext-Funktion (Digest) des**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Servers generiert. Dieser Funktionsaufruf generiert eine Nonce. Dies ist ein eindeutiger Wert, der Informationen enthält, die zum Erkennen von Sicherheitsverletzungen verwendet werden können. Dieser Aufruf generiert auch einen partiellen [*Sicherheitskontext,*](/windows/desktop/SecGloss/s-gly) der zum Verwalten von Zustandsinformationen verwendet wird. Beim Aufrufen **von AcceptSecurityContext (Digest)** geben Sie Kontextanforderungenflags an, um das Verhalten von Microsoft Digest und die Qualität des Schutzes festzulegen. Weitere Informationen finden Sie unter [Digest Challenge Context Requirements](#digest-challenge-context-requirements).

Die Ausgabe des ersten Aufrufs der [**AcceptSecurityContext-Funktion (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) [](/windows/desktop/SecGloss/c-gly) ist ein Sicherheitspuffer, der ein Token enthält, das mit einer HTTP 401-Antwort (Zugriff verweigert) an den Client gesendet wird.

> [!Note]  
> Aufrufe [**von AcceptSecurityContext (Digest),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) die keine Informationen in den Eingabepuffern enthalten, geben eine Digest-Herausforderung zurück.

 

## <a name="digest-challenge-context-requirements"></a>Digest Challenge Context Requirements

Kontextanforderungen sind Flags, die Dies bestimmen:

-   Ob Microsoft Digest als SASL-Mechanismus oder HTTP-Authentifizierungsprotokoll fungiert.
-   Die Qualität des Schutzes, die vom Sicherheitskontext unterstützt wird, der vom Client und Server gemeinsam genutzt wird.

Standardmäßig fungiert Microsoft Digest als SASL-Mechanismus. Um ihn für die HTTP-Authentifizierung zu verwenden, muss das ASC \_ REQ \_ HTTP-Flag (0x10000000) vom Server festgelegt werden.

Kontextanforderungen werden als Flags angegeben, die an den *fContextReq-Parameter* der [**AcceptSecurityContext-Funktion (Digest) übergeben**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) werden. Die Flags beeinflussen die Qualität des Schutzes des Sicherheitskontexts, indem sie die qop-Direktive in der Herausforderung steuern.

Standardmäßig ist die qop-Direktive auf "auth" festgelegt. Um eine Herausforderung zu generieren, die die qop-Direktive auf "auth-int" setzt, muss der Server eines oder mehrere der folgenden Flags angeben:

-   ASC \_ \_ REQ-INTEGRITÄT
-   ASC \_ REQ \_ REPLAY \_ DETECT
-   ASC \_ REQ \_ SEQUENCE \_ DETECT

Nur für SASL: Generieren Sie eine Abfrage, bei der die qop-Direktive auf "auth-conf" festgelegt ist, indem Sie das ASC \_ REQ \_ CONFIDENTIALITY-Kontextanforderungsflag angeben. Da dieses Flag für die HTTP-Authentifizierung nicht gültig ist, kann es nicht mit dem ASC \_ \_ REQ-HTTP-Flag verwendet werden.

Weitere Informationen zur qop-Direktive finden Sie unter [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).

Weitere Informationen zu Herausforderungen finden Sie unter [Inhalt einer Digest-Herausforderung.](contents-of-a-digest-challenge.md)

 

 
