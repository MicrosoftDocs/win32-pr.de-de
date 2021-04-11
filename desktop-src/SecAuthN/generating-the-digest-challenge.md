---
description: Die Microsoft Digest Challenge wird durch den ursprünglichen Rückruf des Servers an die Funktion "akzeptsecuritycontext (Digest)" generiert.
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Die Digest-Abfrage wird erzeugt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511ec4f01c90acf08669835f9728cc711dfd1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217780"
---
# <a name="generating-the-digest-challenge"></a>Die Digest-Abfrage wird erzeugt.

Die Microsoft Digest Challenge wird durch den ursprünglichen Rückruf des Servers an die Funktion " [**akzeptsecuritycontext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " generiert. Dieser Funktions Aufrufwert generiert eine Nonce, bei der es sich um einen eindeutigen Wert handelt, der Informationen enthält, die zum Erkennen von Sicherheitsverletzungen verwendet werden können. Dieser Befehl generiert außerdem einen partiellen [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) , der verwendet wird, um Zustandsinformationen zu verwalten. Beim Aufrufen von " **Accept-SecurityContext (Digest)** " geben Sie kontextanstellungsflags an, um das Verhalten von Microsoft Digest zu steuern und die Qualität des Schutzes festzulegen. Weitere Informationen finden Sie unter [Digest-Abfrage Kontext Anforderungen](#digest-challenge-context-requirements).

Bei der Ausgabe des ersten Aufrufes der [**Accept-SecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) - [*Funktion*](/windows/desktop/SecGloss/c-gly) handelt es sich um einen Sicherheitspuffer, der ein Token enthält, das mit einer HTTP 401-Antwort (Zugriff verweigert) an den Client gesendet wird.

> [!Note]  
> Aufrufe von [**akzeptsecuritycontext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) , die keine Informationen in den Eingabe Puffern enthalten, geben eine Digestherausforderung zurück.

 

## <a name="digest-challenge-context-requirements"></a>Kontext Anforderungen für Digest-Anforderungen

Kontext Anforderungen sind Flags, die Folgendes bestimmen:

-   Gibt an, ob Microsoft Digest als SASL-Mechanismus oder http-Authentifizierungsprotokoll fungiert.
-   Die Qualität des Schutzes, der durch den vom Client und vom Server gemeinsam genutzten Sicherheitskontext unterstützt wird.

Standardmäßig Microsoft Digest Funktionen als SASL-Mechanismus. Um es für die HTTP-Authentifizierung zu verwenden, muss das ASC \_ req \_ http (0x10000000)-Flag vom Server festgelegt werden.

Kontext Anforderungen werden als Flags angegeben, die an den Parameter *fContextReq* der Funktion " [**Accept-SecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " übergeben werden. Die Flags wirken sich auf die Qualität des Sicherheits Kontexts aus, indem Sie die QoP-Direktive in der Herausforderung steuern.

Standardmäßig ist die QoP-Direktive auf "auth" festgelegt. Um eine Aufforderung zu generieren, die die QoP-Direktive auf "auth-int" festlegt, muss der Server mindestens eines der folgenden Flags angeben:

-   ASC \_ req- \_ Integrität
-   ASC \_ req \_ Replay \_ Detect
-   ASC \_ req- \_ Sequenz \_ Erkennung

Nur für SASL: Generieren Sie eine Herausforderung, wenn die QoP-Direktive auf "auth-conf" festgelegt ist, indem Sie das Flag "ASC \_ req \_ Vertraulichkeit Context Requirements" angeben. Da dieses Flag für die HTTP-Authentifizierung nicht gültig ist, kann es nicht mit dem ASC \_ req-http-Flag verwendet werden \_ .

Weitere Informationen zur QoP-Direktive finden Sie unter [Qualität von Schutz und Chiffren](quality-of-protection-and-ciphers.md).

Weitere Informationen zu den Herausforderungen finden Sie unter [Content of a Digest Challenge](contents-of-a-digest-challenge.md).

 

 
