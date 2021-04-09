---
title: Standard Schriftart Objekt
description: Standard Schriftart Objekt
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0fbe2509dd85c1d15b40dc8008dba60d948b5c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039644"
---
# <a name="standard-font-object"></a>Standard Schriftart Objekt

Die standardmäßige ambient-Schriftart Eigenschaft, die vom Container bereitgestellt wird, und die Standard Schriftart Eigenschaft, die vom-Steuerelement bereitgestellt wird, stellen ein Standardschrift Das heißt, dass diese Standard Schriftarten einen **IDispatch** -Zeiger auf ein Standard schriftobjekt bereitstellen.

Das Font-Objekt ist eine vom System bereitgestellte Implementierung eines Satzes von Schnittstellen oberhalb der zugrunde liegenden GDI-Schriftart Unterstützung. Ein Schriftart Objekt wird über die API-Funktion [**olecreatefontindirekt**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) mit einer [**fontdebug**](/windows/win32/api/olectl/ns-olectl-fontdesc) -Struktur erstellt. Das Font-Objekt unterstützt eine Reihe von Lese-/Schreibeigenschaften sowie benutzerdefinierte Methoden über die Schnittstelle [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)und unterstützt denselben Satz von Eigenschaften (aber nicht die Methoden) über eine "dispinterface"- [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). Die dispinterface wird für die zuvor erwähnten Schriftart Eigenschaften verwendet. Die Eigenschaften entsprechen den GDI-Schriftart Attributen, die in der [**LOGFONT**](/windows/win32/api/dimm/ns-dimm-logfonta) -Struktur beschrieben werden.

Das Schriftart Objekt unterstützt auch die ausgehende Schnittstelle [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) , damit ein Client ermitteln kann, wann die Schriftart Eigenschaften geändert werden. Da das Font-Objekt mindestens eine ausgehende Schnittstelle unterstützt, implementiert es zu diesem Zweck auch [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) und einen Verbindungspunkt für **IPropertyNotifySink** .

Das Font-Objekt stellt eine hFont-Eigenschaft bereit, bei der es sich um ein Windows-Schriftart Handle handelt, das den anderen für die Schriftart angegebenen Attributen entspricht. Das Schriftart Objekt verzögert das Erkennen dieser Schriftart, wenn möglich, sodass das Festlegen von zwei Eigenschaften für eine Schriftart nicht dazu führt, dass eine zwischen Schriftart realisiert wird. Außerdem verwaltet das Standard Schriftart Objekt als Optimierung einen Cache von Schriftart Handles. Zwei Schriftart Objekte im gleichen Prozess mit identischen Eigenschaften geben das gleiche Schriftart Handle zurück. Mit dem Font-Objekt können Schriftarten aus diesem Cache nach Bedarf entfernt werden. Dies führt zu speziellen Überlegungen für Clients, die diese hFont-Eigenschaft verwenden. Weitere Informationen finden [**Sie unter IFont:: get \_ hFont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) .

Das Schriftart Objekt unterstützt auch [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , sodass es sich selbst speichern und aus einer Instanz von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)laden kann. Alle anderen Objekte, die intern ein Schriftart Objekt verwenden, speichern und laden die Schriftart normalerweise als Teil der eigenen persistenzverarbeitung des Objekts.

Außerdem unterstützt das Font-Objekt [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , über das es einen Eigenschaften Satz mit typisierten Werten für jede Schriftart Eigenschaft bereitstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Eigenschaften](control-properties.md)
</dt> </dl>

 

 