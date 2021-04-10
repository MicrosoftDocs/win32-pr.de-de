---
title: Persistenz
description: Persistenz
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5fc0c8e389c7babdf80b76719b39fc02d5604
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039704"
---
# <a name="persistence"></a>Persistenz

Ein Steuerelement implementiert eine oder mehrere der persistenzschnittstellen, um die Persistenz seines Zustands zu unterstützen. Beispielsweise unterstützt die [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) -Schnittstelle die streambasierte Persistenz des Zustands des Steuer Elements. **IPersistStreamInit** ist ein Ersatz für [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) und fügt eine Initialisierungs Methode, [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew), hinzu. Die anderen Methoden sind in beiden Schnittstellen identisch. **IPersistStreamInit** ist nicht von **IPersistStream** abgeleitet. ein-Objekt unterstützt nur eine der beiden Schnittstellen, je nachdem, ob es die Möglichkeit erfordert, neue Instanzen von sich selbst zu initialisieren.

Zu den anderen persistenzschnittstellen, die ein Steuerelement anbieten kann, gehören: [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**ipersistmemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), [**ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). Die Implementierung des Steuer Elements muss entscheiden, welche Arten von Persistenz am wichtigsten sind, und die entsprechenden persistenzschnittstellen implementieren. Die Implementierung des Steuer Elements entscheidet auch, was gespeichert werden soll. Ein Steuerelement kann z. b. die aktuellen Werte der zugehörigen Eigenschaften oder deren Position und Größe in seinem Container speichern. Der Client entscheidet, welche Schnittstelle er bevorzugt verwenden soll.

Bevor ein-Steuerelement aus seinem permanenten Zustand geladen wird, kann ein Client das OLEMISC \_ setclientsitefirst-Flag überprüfen, um zu bestimmen, ob das Steuerelement das Aufrufen seiner Client Site und Ambient-Eigenschaften vor dem Laden seines permanenten Zustands unterstützt. Diese Optimierung kann Zeit sparen, wenn ein Steuerelement instanziiert wird, da das Steuerelement dann seine permanenten Werte ignorieren kann, anstatt Sie nur zu laden, damit Sie von Umgebungs Eigenschaften, die vom Client bereitgestellt werden, überschrieben werden.

Ein Steuerelement kann auch das Speichern und Wiederherstellen seines Zustands in einem OLE-Eigenschaften Satz, einem Satz von bezeichnerwerten und Werten in einem angegebenen Format unterstützen. Diese Funktion kann für Container wie Visual Basic nützlich sein, die ihre Programme in Textform speichert. Ein Steuerelement, das diese Funktion unterstützen möchte, implementiert [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) und [**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) , um die Eigenschaftswerte an bzw. aus dem Container zu übergeben. Es ist die Aufgabe des Containers, diese Informationen in Text zu konvertieren und zu speichern. Die vom Steuerelement verwendeten Bezeichner entsprechen den Eigenschaften Namen und den Werten des Steuer Elements. Sehen Sie sich das OLE CDK für die Definition dieses Eigenschaften Satzes an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 