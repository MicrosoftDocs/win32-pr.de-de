---
description: Sie können verhindern, dass nicht autorisierte Benutzer Ereignisse empfangen, auf die Sie keinen Zugriff haben sollen.
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: Sicheres Bereitstellen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217400"
---
# <a name="providing-events-securely"></a>Sicheres Bereitstellen von Ereignissen

Sie können verhindern, dass nicht autorisierte Benutzer Ereignisse empfangen, auf die Sie keinen Zugriff haben sollen. Der Ereignis Anbieter kann Instanzen seiner eigenen Ereignis Klassen bereitstellen, so wie der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) Klassen wie z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)bereitstellt. Der Ereignis Anbieter kann auch systeminterne Ereignisse bereitstellen, z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md). Weitere Informationen finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).

Ein Ereignis Anbieter kann den Zugriff auf Ereignis Empfänger wie folgt steuern:

-   Die Verwendung der Zugriffs Steuerung durch Implementieren von [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) ist die effizienteste Methode.

    Der Anbieter bestimmt, ob der Consumer über Berechtigungen zum Empfangen eines angeforderten Ereignisses verfügt. Wenn dem Consumer keine ausreichenden Berechtigungen zum Registrieren fehlen, gibt WMI einen Fehler vom Typ "Zugriff verweigert" zurück. Verwenden Sie diesen Modus, wenn der Anbieter entscheiden kann, wer Ereignisse empfangen kann. Ein Anbieter kann z. b. sicherheitsrelevante Ereignisse bereitstellen, und es kann erforderlich sein, dass der Consumer über Administratorrechte mit aktivierter Berechtigung " **SeSecurityPrivilege** " verfügt.

-   Das Implementieren von [**iwbemeventsink:: setsinksecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) in der Senke, die zum Aufrufen von Ereignissen verwendet wird, ermöglicht die Einstellung einer Sicherheits Beschreibung (SD) auf einer Senke für alle Ereignisse, die durchlaufen werden.

    WMI führt Zugriffs Überprüfungen auf der Grundlage der SD aus. Verwenden Sie diesen Modus, wenn der Anbieter nicht entscheiden kann, wer seine Ereignisse verwenden darf, sondern eine SD-Entscheidung für eine bestimmte Senke treffen kann. Verwenden Sie z. b. [**iwbemeventsink:: setsink Security**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) , wenn der Ereignis Anbieter mehrere senken durch Aufrufe von [**iwbemeventsink:: getrestrictedsink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) abgerufen hat und Sie eine Sicherheits Beschreibung für jede Senke verwenden möchten.

-   Durch Festlegen **der \_ sicherheitsbeschreibungenschaft** eines Ereignisses wird die Einstellung einer SD für jedes Ereignis ermöglicht.

    Verwenden Sie diesen Ansatz, wenn jedes Ereignis, das an die Senke gesendet wird, unterschiedliche Sicherheits Beschreibungen aufweisen kann. Zum Verwenden dieses Ansatzes leiten Sie eine der vom Anbieter definierten System externe-Ereignis Klassen von [**\_ \_ Event**](--event.md) oder [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) ab, sodass die Klasse die **\_ sicherheitsbeschreibungenschaft** enthält. Beispielsweise kann der Ereignis Anbieter sichere und normale Ereignisse über eine Senke veröffentlichen. Verwenden Sie in diesem Fall die Sicherheits Beschreibung des Administratoren Kontos für sichere Ereignisse und eine **null** -Sicherheits Beschreibung für normale Ereignisse, die von jedermann empfangen werden können.

## <a name="securing-events-by-decoupled-event-providers"></a>Sichern von Ereignissen durch entkoppelte Ereignis Anbieter

Entkoppelte Ereignis Anbieter unterscheiden sich von nicht entkoppelten Ereignis Anbietern in der Art und Weise, wie Sie sich bei WMI registrieren. Beim Aufrufen von [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) für Ereignisse eines entkoppelten Anbieters wird das Client Zugriffs Token nie weitergegeben. WMI behandelt die Zugriffs Steuerung auf die gleiche Weise wie für nicht entkoppelte Ereignis Anbieter. Weitere Informationen zum Schreiben eines entkoppelten Anbieters finden Sie unter [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md).

Nur Administratoren mit dem **vollständigen \_ Schreib** Zugriff, die in der **WMI-Steuerung** der **Systemsteuerung** festgelegt sind, können Ereignisse für einen Namespace hervorrufen. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> </dl>

 

 
