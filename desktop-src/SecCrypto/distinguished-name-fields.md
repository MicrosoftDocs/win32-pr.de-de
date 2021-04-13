---
description: Enthält Informationen, die die Person, die die Anforderung stellt, eindeutig identifizieren sollten.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Felder für Distinguished Name
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a03495d19608e29aa60f09954c96a10f6c3cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529084"
---
# <a name="distinguished-name-fields"></a>Felder für Distinguished Name

Eine [*Zertifikat Anforderung*](../secgloss/c-gly.md) enthält Informationen, mit denen die Person, die die Anforderung sendet, eindeutig identifiziert werden soll.

PKCS \# 10-Formatierungs Zertifikat Anforderungen, die von den Zertifikat Diensten akzeptiert werden, enthalten identifikationsfelder, die als DN-Felder (Distinguished Name) bezeichnet werden. Diese Felder enthalten die Informationen, die vom Benutzer eingegeben werden, wenn eine Zertifikat Anforderung von Key Manager, der Zertifikats Registrierungs [Steuerung](certificate-enrollment-control.md)oder einer anderen Methode erstellt wird.

Im folgenden finden Sie einige Richtlinien für den Abschluss der DN-Felder in einer Zertifikat Anforderung.



| Feld               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allgemeiner Name         | Benutzerzertifikate: Geben Sie den vollständigen Namen der Person ein. Computer Zertifikate: Geben Sie den voll qualifizierten *Hostnamen *- **/** _Pfad_ ein, der in DNS-Suchen verwendet wird, auf denen der Server ausgeführt wird (z *. b. Hostname *)**.** _Beispiel_* _. com_*).<br/>                                                                                                  |
| Organization        | Der Name, den Sie für das Feldorganisation angeben, sollte der rechtliche Name für Ihre Organisation sein, der in der entsprechenden Stadt, Bundesland oder Land/Region registriert ist. Der rechtliche Name der Organisation muss im Feldorganisation verwendet werden.                                                                                                      |
| Organizational Unit | Das Feld Organisationseinheit kann verwendet werden, um zwischen verschiedenen Abteilungen innerhalb einer Organisation zu unterscheiden, z. b. "Internet Sicherheitseinheit" oder "Personalwesen". Dieses Feld wird auch zum Angeben eines DBA-Werts (Business as...) verwendet.                                                                                           |
| Ort            | Das Feld "Ort" bezeichnet die Stadt, in der sich die Organisation befindet. Wenn die Organisation nur über lokale Unternehmen verfügt, weil eine Geschäftslizenz bei der Stadt Clerk für die Stadt "Cambridge" im Bundesstaat Massachusetts registriert ist, muss das Feld "Ort" Cambridge enthalten.                                                                |
| Bundesland oder Kanton   | Das Feld Bundesland oder Kanton gibt an, wo sich die Organisation physisch befindet. Wenn Ihre Organisation in Delaware integriert ist, aber einen DBA (Business as...) in Kalifornien hat, verwenden Sie Kalifornien. Das Feld "State" oder "Province" sollte kein abgekürzte Feld sein. Beispielsweise ist "ca" kein gültiger Zustands Name. "California" ist der richtige Zustands Name. |
| Land/Region      | Der [*X. 500*](../secgloss/x-gly.md) -Benennungs Schema-Standard erfordert einen 2-stelligen Länder-/Regionscode. Der Länder-/Regionscode für den USA ist "US;". der Länder-/Regionscode für Kanada ist ca.                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Namens Eigenschaften](name-properties.md)
</dt> </dl>

 

 
