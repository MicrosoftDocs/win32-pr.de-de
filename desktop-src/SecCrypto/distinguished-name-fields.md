---
description: Enthält Informationen, die die Person, die die Anforderung stellt, eindeutig identifizieren sollen.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Distinguished Name-Felder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10465a481c1efbaa9637979bb5bb82880451fbe43800b968a4c9fefc5fbc4a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767265"
---
# <a name="distinguished-name-fields"></a>Distinguished Name-Felder

Eine [*Zertifikatanforderung*](../secgloss/c-gly.md) enthält Informationen, die die Person, die die Anforderung stellt, eindeutig identifizieren sollten.

Zertifikatanforderungen im PKCS \# 10-Format, die von Zertifikatdiensten akzeptiert werden, enthalten Identifikationsfelder, die als DN-Felder (Distinguished Name) bezeichnet werden. Diese Felder enthalten die Informationen, die vom Benutzer eingegeben werden, wenn eine Zertifikatanforderung vom Schlüssel-Manager, [der Zertifikatregistrierungssteuerung](certificate-enrollment-control.md)oder einer anderen Möglichkeit erstellt wird.

Im Folgenden sind einige Richtlinien für die Vervollständigung von DN-Feldern in einer Zertifikatanforderung enthalten.



| Feld               | Beschreibung                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allgemeiner Name         | Benutzerzertifikate: Geben Sie den vollständigen Namen der Person ein. Computerzertifikate: Geben Sie den vollqualifizierten *HostName*-Pfad **/**  ein, der in DNS-Suchläufen verwendet wird, auf denen der Server ausgeführt wird (z. B. *HostName*). _Beispiel_* _.com_*).<br/>                                                                                                  |
| Organization        | Der Name, den Sie für das Feld Organisation angeben, sollte der rechtliche Name für Ihre Organisation sein, der bei der entsprechenden Stadt, dem entsprechenden Bundesland oder der entsprechenden Autorität für Land/Region registriert ist. Der rechtliche Name der Organisation muss im Feld Organisation verwendet werden.                                                                                                      |
| Organizational Unit | Das Feld Organisationseinheit kann verwendet werden, um zwischen verschiedenen Abteilungen innerhalb einer Organisation zu unterscheiden, z.B. "Internetsicherheitseinheit" oder "Personalwesen". Dieses Feld wird auch für die Angabe eines DBA-Werts (Doing Business As...) empfohlen.                                                                                           |
| Ort            | Das Feld Lokalität gibt die Stadt an, in der sich die Organisation befindet. Wenn die Organisation nur ortsansässig ist, weil eine Geschäftslizenz beim City Clerk für die City ofSpezifik in der State of Bostons registriert ist, muss das Feld Locality (Ort) Den Ort (Ort) enthalten.                                                                |
| Bundesland oder Kanton   | Das Feld State or Province gibt an, wo sich die Organisation physisch befindet. Wenn Ihre Organisation in Delaware integriert ist, aber über einen DBA (Doing Business As...) in Kalifornien verfügt, verwenden Sie Kalifornien. Das Feld State oder Province darf kein abgekürztes Feld sein. "CA" ist beispielsweise kein gültiger Statusname. "California" ist der richtige Bundesstaatsname. |
| Land/Region      | Der [*X.500*](../secgloss/x-gly.md) Naming Scheme-Standard erfordert einen zweistelligen Länder-/Regionscode. Der Länder-/Regionscode für die USA ist "USA". Der Länder-/Regionscode für Kanada lautet CA.                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Namenseigenschaften](name-properties.md)
</dt> </dl>

 

 
