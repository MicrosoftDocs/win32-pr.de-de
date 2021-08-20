---
title: Standardschriftartobjekt
description: Standardschriftartobjekt
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1beb4ac2890cd3314c1b23f847192f1d3248b02e301c27d5990f524c74c0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104153"
---
# <a name="standard-font-object"></a>Standardschriftartobjekt

Die vom Container bereitgestellte Standard-Ambient-Schriftarteigenschaft und die vom -Steuerelement bereitgestellte Standardschriftarteigenschaft stellen beide ein Standardschriftartobjekt bereit. Das heißt, diese Standardschriftarten stellen einen **IDispatch-Zeiger** auf ein Standardschriftartobjekt bereit.

Das Schriftartobjekt ist eine vom System bereitgestellte Implementierung eines Satzes von Schnittstellen über der zugrunde liegenden GDI-Schriftartunterstützung. Ein Schriftartobjekt wird mithilfe der API-Funktion [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) erstellt, wenn eine [**FONTDESC-Struktur**](/windows/win32/api/olectl/ns-olectl-fontdesc) angegeben wird. Das Schriftartobjekt unterstützt über die [**Schnittstelle IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)eine Reihe von Lese-/Schreibeigenschaften sowie benutzerdefinierte Methoden und über eine [**Disp-Schnittstelle IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)den gleichen Satz von Eigenschaften (aber nicht die Methoden). Die Disp-Schnittstelle wird für die zuvor erwähnten Schriftarteigenschaften verwendet. Die Eigenschaften entsprechen den GDI-Schriftartattributen, die in der [**LOGFONT-Struktur**](/windows/win32/api/dimm/ns-dimm-logfonta) beschrieben werden.

Das Schriftartobjekt unterstützt auch die ausgehende Schnittstelle [**IPropertyNotifySink, sodass**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) ein Client bestimmen kann, wann sich Schriftarteigenschaften ändern. Da das Schriftartobjekt mindestens eine ausgehende Schnittstelle unterstützt, implementiert es zu diesem Zweck auch [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) und einen Verbindungspunkt für **IPropertyNotifySink.**

Das Schriftartobjekt stellt eine hFont-Eigenschaft bereit, die ein Windows Schriftarthandle ist, das den anderen für die Schriftart angegebenen Attributen entspricht. Das Schriftartobjekt verzögert das Erkennen dieser Schriftart, wenn möglich, sodass das aufeinanderfolgende Festlegen von zwei Eigenschaften für eine Schriftart nicht dazu führt, dass eine Zwischenschriftart realisiert wird. Darüber hinaus verwaltet das Standardschriftartobjekt als Optimierung einen Cache von Schriftarthandles. Zwei Schriftartobjekte im selben Prozess, die über identische Eigenschaften verfügen, geben das gleiche Schriftarthandle zurück. Das Schriftartobjekt kann Schriftarten nach Bekunden aus diesem Cache entfernen, was besondere Überlegungen für Clients einführt, die diese hFont-Eigenschaft verwenden. Weitere Informationen finden Sie unter [**IFont::get \_ hFont.**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont)

Das Schriftartobjekt unterstützt auch [**IPersistStream,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) sodass es sich selbst in einer Instanz von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)speichern und laden kann. Jedes andere Objekt, das intern ein Schriftartobjekt verwendet, würde normalerweise die Schriftart im Rahmen der eigenen Persistenzbehandlung des Objekts speichern und laden.

Darüber hinaus unterstützt das Schriftartobjekt [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) über das es einen Eigenschaftensatz mit typisierten Werten für jede Schriftarteigenschaft bereitstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementeigenschaften](control-properties.md)
</dt> </dl>

 

 