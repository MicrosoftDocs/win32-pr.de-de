---
title: Datenbindung über IPropertyNotifySink
description: Datenbindung über IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d39c7277d27f0df6c185fc35a926aa98b77b91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714262"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Datenbindung über IPropertyNotifySink

Objekte, die Eigenschaften unterstützen, z. b. über die OLE-Automatisierung und die **IDispatch** -Schnittstelle, möchten möglicherweise, dass Clients benachrichtigt werden, wenn bestimmte Eigenschaften den Wert ändern. Eine solche Eigenschaft wird als bindbare Eigenschaft bezeichnet, da die Benachrichtigungen es einem Client ermöglichen, seine eigene Anzeige der aktuellen Eigenschaftswerte des Objekts zu synchronisieren. Außerdem kann es sein, dass ein Client die gleichen Objekte steuern kann, wenn bestimmte Eigenschaften geändert werden dürfen. Diese Eigenschaften werden als Eigenschaften für die Anforderungs Bearbeitung bezeichnet.

[**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) ist eine Standard Benachrichtigungs Schnittstelle, die bindbare und Anforderungs Bearbeitungseigenschaften unterstützt. **IPropertyNotifySink** wird von einem Objekt mit Eigenschaften als ausgehende Schnittstelle unterstützt. Das heißt, die Schnittstelle selbst wird durch das Senkenobjekt eines Clients implementiert, und der Client verbindet die Senke über den zuvor beschriebenen Verbindungspunkt Mechanismus mit dem unterstützenden Objekt. **IPropertyNotifySink** ist wie folgt definiert:

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Wenn ein Objekt seine verbundenen senken Benachrichtigen möchte, dass eine bindbare Eigenschaft, die mit einer bestimmten DISPID identifiziert wurde, geändert wurde, ruft es [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged)auf. Wenn ein Objekt mehrere Eigenschaften gleichzeitig ändert, kann es "DISPID \_ unknown" an " **OnChanged** " übergeben. in diesem Fall aktualisiert der Client den Cache aller Eigenschaftswerte, die von Interesse sind.

Wenn eine Eigenschaft zum Bearbeiten der Anforderung geändert wird, kann ein Objekt den Client bitten, den Client so zu ändern, dass er diese Änderung zulässt. Das Objekt ruft [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) auf und übergibt die DispID der fraglichen Eigenschaft (oder DISPID \_ unbekannt, um alle Eigenschaften zu identifizieren). Die Senke des Clients gibt s \_ OK zurück, um anzugeben, dass die Änderung zulässig ist, oder s \_ false (oder einen Fehler), um anzugeben, dass eine Änderung nicht zulässig ist. Wenn ein Objekt **OnRequestEdit** aufruft, müssen die Anforderungen des Clients befolgt werden, indem die genaue Semantik der ' false ' \_ -und ' \_ false '-Rückgabewerte befolgt wird.

Beachten Sie, dass " [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) " nicht zur Datenüberprüfung verwendet werden kann, da der neue Wert der Eigenschaft zum Zeitpunkt des Aufrufes noch nicht verfügbar ist. Die Benachrichtigung kann nur zum Steuern eines schreibgeschützten Zustands für eine Eigenschaft verwendet werden.

-Objekte steuern, welche Eigenschaften gebunden werden können und wie Sie diese Eigenschaften in den Typinformationen des Objekts bearbeiten und markieren. In den Typinformationen markiert das Attribut bindbare eine Eigenschaft als Unterstützung von [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). Das Attribut requestedit markiert eine Eigenschaft als Unterstützung von [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit).

Eine Eigenschaft kann beide Verhalten unterstützen. in diesem Fall wird [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) zuerst aufgerufen, und nur wenn die Änderung zulässig ist, wird " [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) " aufgerufen.

Die einzige Ausnahme beim Verhalten solcher Eigenschaften besteht darin, dass keine Benachrichtigungen als Ergebnis der Initialisierungs-oder lade Prozeduren eines Objekts gesendet werden. Dabei wird davon ausgegangen, dass alle Eigenschaften geändert werden und dass alle geändert werden dürfen. Benachrichtigungen an diese Schnittstelle sind daher nur im Kontext eines vollständig initialisierten/geladenen Objekts sinnvoll.

Zwei weitere Attribute können auf Eigenschaften in den Typinformationen eines Objekts angewendet werden. Das Defaultbind-Attribut kennzeichnet eine bindbare Eigenschaft als eine Eigenschaft, die den Status des Objekts als Ganzes am besten darstellt. Das Display BIND-Attribut markiert eine bindbare Eigenschaft, die für die Anzeige in der eigenen Benutzeroberfläche eines Clients geeignet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften Seiten und Eigenschaften Blätter](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




