---
title: Datenbindung über IPropertyNotifySink
description: Datenbindung über IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337233455872928f824d8cbb903aba247b1ef496d02c0af04223361731fe3663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854650"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Datenbindung über IPropertyNotifySink

Objekte, die Eigenschaften unterstützen, z. B. über OLE-Automatisierung und die **IDispatch-Schnittstelle,** möchten möglicherweise clients die Benachrichtigung ermöglichen, wenn bestimmte Eigenschaften den Wert ändern. Eine solche Eigenschaft wird als bindbare Eigenschaft bezeichnet, da die Benachrichtigungen es einem Client ermöglichen, seine eigene Anzeige der aktuellen Eigenschaftswerte des Objekts zu synchronisieren. Darüber hinaus möchten dieselben Objekte einem Client möglicherweise ermöglichen, zu steuern, wann bestimmte Eigenschaften geändert werden dürfen. Solche Eigenschaften werden als Anforderungsbearbeitungseigenschaften bezeichnet.

[**IPropertyNotifySink ist eine**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) Standard-Benachrichtigungsschnittstelle, die bindbare Eigenschaften und Eigenschaften zum Bearbeiten von Anforderungen unterstützt. **IPropertyNotifySink** wird von einem Objekt mit Eigenschaften als ausgehende Schnittstelle unterstützt. Das heißt, die Schnittstelle selbst wird durch das Senkenobjekt eines Clients implementiert, und der Client verbindet die Senke über den zuvor beschriebenen Verbindungspunktmechanismus mit dem unterstützenden Objekt. **IPropertyNotifySink** ist wie folgt definiert:

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Wenn ein Objekt seine verbundenen Senken benachrichtigen möchte, dass eine bindbare Eigenschaft, die mit einer angegebenen DISPID identifiziert wurde, geändert wurde, ruft es [**OnChanged auf.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) Wenn ein Objekt mehrere Eigenschaften gleichzeitig ändert, kann es DISPID UNKNOWN an \_ **OnChanged** übergeben. In diesem Fall aktualisiert ein Client seinen Cache aller für ihn wichtigen Eigenschaftswerte.

Wenn sich eine Anforderungsbearbeitungseigenschaft ändert, kann ein Objekt den Client fragen, ob diese Änderung zulässig ist. Das -Objekt ruft [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) auf und überträgt die DISPID der in Frage gestellten Eigenschaft (oder DISPID \_ UNKNOWN, um alle Eigenschaften zu identifizieren). Die Senke des Clients gibt S OK zurück, um anzugeben, dass die Änderung zulässig ist, oder S FALSE (oder ein Fehler), um anzugeben, dass \_ die Änderung nicht zulässig \_ ist. Wenn ein Objekt **OnRequestEdit** aufruft, muss es den Wünschen des Clients folgen, indem die genaue Semantik der Rückgabewerte S OK und \_ S FALSE befolgt \_ wird.

Beachten [**Sie, dass OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) nicht für die Datenüberprüfung verwendet werden kann, da zum Zeitpunkt des Aufrufs der neue Wert der -Eigenschaft noch nicht verfügbar ist. Die Benachrichtigung kann nur verwendet werden, um einen schreibgeschützten Zustand für eine Eigenschaft zu steuern.

Objekte steuern, welche Eigenschaften bindbar sind, fordern eine Bearbeitung an und markieren solche Eigenschaften in den Typinformationen des Objekts. In den Typinformationen markiert das bindbare Attribut eine Eigenschaft als unterstützend [**für OnChanged.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) Das Attribut requestedit markiert eine Eigenschaft als unterstützend [**für OnRequestEdit.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit)

Eine Eigenschaft kann beide Verhaltensweisen unterstützen, in diesem Fall [**wird OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) zuerst aufgerufen, und nur wenn eine Änderung zulässig ist, wird [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) aufgerufen.

Die einzige Ausnahme beim Verhalten solcher Eigenschaften ist, dass keine Benachrichtigungen als Ergebnis der Initialisierungs- oder Ladevorgänge eines Objekts gesendet werden. In solchen Fällen wird davon ausgegangen, dass sich alle Eigenschaften ändern und alle geändert werden dürfen. Benachrichtigungen an diese Schnittstelle sind daher nur im Kontext eines vollständig initialisierten/geladenen Objekts sinnvoll.

Zwei weitere Attribute können auf Eigenschaften in den Typinformationen eines Objekts angewendet werden. Das defaultbind-Attribut markiert eine bindbare Eigenschaft als die Eigenschaft, die den Zustand des Objekts als Ganzes am besten darstellt. Das attribut displaybind markiert eine bindbare Eigenschaft als für die Anzeige auf der eigenen Benutzeroberfläche eines Clients geeignet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaftenseiten und Eigenschaftenblätter](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




