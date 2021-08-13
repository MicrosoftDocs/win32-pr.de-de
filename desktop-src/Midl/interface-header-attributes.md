---
title: Schnittstellenheaderattribute
description: Integrieren Sie diese Attribute in den Schnittstellenheader, um Informationen über die gesamte Schnittstelle zu übermitteln.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL , Attribute, Schnittstellenheader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26dac473c95625162e6dbb689f54833a166b1c58ae478654c52fededf3dd529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642986"
---
# <a name="interface-header-attributes"></a>Schnittstellenheaderattribute

Integrieren Sie diese Attribute in den Schnittstellenheader, um Informationen über die gesamte Schnittstelle zu übermitteln.



| attribute                                   | Verbrauch                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async \_ uuid**](async-uuid.md)           | Weist den MIDL-Compiler an, sowohl synchrone als auch asynchrone Versionen einer COM-Schnittstelle zu definieren.                                                                                                                                               |
| [**Uuid**](uuid.md)                        | Legt einen 128-Bit-Wert fest, der eine bestimmte Schnittstelle von allen anderen unterscheidet. Der tatsächliche Wert kann eine GUID, eine CLSID oder eine IID darstellen.                                                                                                 |
| [**local**](local.md)                      | Weist den MIDL-Compiler an, nur Headerdateien zu generieren. Eine Schnittstelle muss entweder über ein [**uuid-**](uuid.md) oder ein [**lokales**](local.md) Attribut verfügen.                                                                                             |
| [**ms \_ union**](-ms-union.md)              | Steuert die NDR-Ausrichtung nicht gekapselter Unions. Verwenden Sie aus Gründen der Abwärtskompatibilität mit Schnittstellen, die auf MIDL 1.0 oder 2.0 aufbauen.                                                                                                                   |
| [**Objekt (object)**](object.md)                    | Identifiziert die Schnittstelle als COM-Schnittstelle und weist den MIDL-Compiler an, Proxy-/Stubcode anstelle von RPC-Client- und -Serverstubs zu generieren.                                                                                                    |
| [**Version**](version.md)                  | Identifiziert eine bestimmte Version einer Schnittstelle in Fällen, in denen mehrere Versionen der Schnittstelle vorhanden sind. Da COM-Schnittstellen unveränderlich sind, [](version.md) können Sie das Versionsattribut nicht für eine [**Objektschnittstelle**](object.md) verwenden. |
| [**\_Zeigerstandard**](pointer-default.md) | Gibt den Standardzeigertyp für alle Zeiger mit Ausnahme der in Parameterlisten enthaltenen Zeiger an. Der Standardtyp kann [**eindeutig,**](unique.md) [**ref**](ref.md)oder [**ptr**](ptr.md)sein.                                                   |
| [**Endpunkt**](endpoint.md)                | Gibt einen statischen (bekannten) Endpunkt an, auf dem eine Serveranwendung auf Remoteprozeduraufrufe lauscht.                                                                                                                                   |



 

Unter [Type Library Attributes (Typbibliotheksattribute)](type-library-attributes.md) finden Sie Schnittstellenattribute wie [**dual**](dual.md) und [**oleautomation,**](oleautomation.md)die spezifisch für Schnittstellen sind, die in einer Bibliotheks-Anweisung definiert sind oder auf die verwiesen wird.

 

 




