---
title: Schnittstellen Header Attribute
description: Fügen Sie diese Attribute in den Schnittstellen Header ein, um Informationen über die gesamte-Schnittstelle zu übermitteln.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL-Mittell, Attribute, Schnittstellen Header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036768"
---
# <a name="interface-header-attributes"></a>Schnittstellen Header Attribute

Fügen Sie diese Attribute in den Schnittstellen Header ein, um Informationen über die gesamte-Schnittstelle zu übermitteln.



| Attribut                                   | Verbrauch                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Async- \_ UUID**](async-uuid.md)           | Weist den Mittel l-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.                                                                                                                                               |
| [**UUID**](uuid.md)                        | Legt einen 128-Bit-Wert fest, der eine bestimmte Schnittstelle von allen anderen unterscheidet. Der tatsächliche Wert kann eine GUID, eine CLSID oder eine IID darstellen.                                                                                                 |
| [**nah**](local.md)                      | Weist den Mittel l-Compiler an, nur Header Dateien zu generieren. Eine Schnittstelle muss entweder ein [**UUID**](uuid.md) -oder ein [**Lokales**](local.md) Attribut haben.                                                                                             |
| [**MS- \_ Union**](-ms-union.md)              | Steuert die NDR-Ausrichtung von nicht gekapselten Unions. Verwenden Sie aus Gründen der Abwärtskompatibilität mit Schnittstellen, die auf mittlerer l 1,0 oder 2,0 basieren.                                                                                                                   |
| [**Objekt (object)**](object.md)                    | Identifiziert die-Schnittstelle als COM-Schnittstelle und leitet den Mittelwert Compiler an die Generierung von Proxy-/Stubcode anstelle von RPC-Client-und Serverstubs weiter.                                                                                                    |
| [**version**](version.md)                  | Identifiziert eine bestimmte Version einer Schnittstelle in Fällen, in denen mehrere Versionen der Schnittstelle vorhanden sind. Da com-Schnittstellen unveränderlich sind, können Sie das [**Versions**](version.md) Attribut nicht in einer [**Objekt**](object.md) Schnittstelle verwenden. |
| [**Zeiger \_ Standard**](pointer-default.md) | Gibt den Standard Zeigertyp für alle Zeiger außer den in Parameterlisten enthaltenen Zeigern an. Der Standardtyp kann [**eindeutig**](unique.md), [**ref**](ref.md)oder [**ptr**](ptr.md)sein.                                                   |
| [**Dreher**](endpoint.md)                | Gibt einen statischen (bekannten) Endpunkt an, auf dem eine Serveranwendung auf Remote Prozedur Aufrufe lauschen soll.                                                                                                                                   |



 

Siehe [Typbibliotheks Attribute](type-library-attributes.md) für Schnittstellen Attribute, z. b. [**Dual**](dual.md) und [**oleautomation**](oleautomation.md), die spezifisch für Schnittstellen sind, die in einer Bibliotheks Anweisung definiert sind oder auf die verwiesen wird.

 

 




