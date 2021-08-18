---
title: Implementieren der Eigenschaftenseite für ein DSP-Plug-In
description: Implementieren der Eigenschaftenseite für ein DSP-Plug-In
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Windows Media Player-Plug-Ins, Audio-DSP
- Plug-Ins, Audio-DSP
- Digitale Signalverarbeitungs-Plug-Ins, Audioeigenschaften
- DSP-Plug-Ins, Audioeigenschaften
- Audio-DSP-Plug-Ins, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac64dbd1e984d649a4405341d907ddd0c93eabce855bed90e83f698b778a3a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617310"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implementieren der Eigenschaftenseite für ein DSP-Plug-In

Windows Media Player können eine Eigenschaftenseite für jedes DSP-Plug-In anzeigen, damit Benutzer Werte festlegen können, die das Verhalten des Plug-Ins ändern. Benutzer können über die Registerkarte **Plug-Ins** des Dialogfelds Optionen auf die Eigenschaftenseite zugreifen, indem sie auf den Namen des DSP-Plug-Ins klicken, um es auszuwählen, und dann auf **Eigenschaften** klicken.

Der Beispielcode des Windows Media Player-Plug-In-Assistenten stellt eine Standardimplementierungen einer Eigenschaftenseite bereit, die ein einzelnes Bearbeitungsfeld enthält, das vom Benutzer einen Wert empfängt, der einen Skalierungsfaktor für die Audiolautstärke darstellt. Wenn der Benutzer auf **Anwenden** klickt, übergibt die Eigenschaftenseite diesen Wert an das Plug-In-Objekt, damit das Plug-In den Wert ändern kann, der zum Skalieren des Volumes während der Verarbeitung verwendet wird.

## <a name="about-the-property-page-object"></a>Informationen zum Eigenschaftenseitenobjekt

Das Eigenschaftenseitenobjekt ist ein COM-Objekt, das die **IPropertyPage-Schnittstelle** implementiert. Der vom Plug-In-Assistenten generierte Beispielcode verwendet die ATL-Implementierung von **IPropertyPage,** die in der Visual C++-Dokumentation auf MSDN dokumentiert ist. Ihr Code sollte mindestens Überschreibungsimplementierungen für **IPropertyPage::OnInitDialog** bereitstellen, das das Ereignis behandelt, das beim Öffnen der Eigenschaftenseite auftritt, und **IPropertyPage::Apply**, das das Ereignis behandelt, das auftritt, wenn der Benutzer auf **Anwenden** klickt. Der Plug-In-Assistent generiert Beispielcode für jeden dieser Ereignishandler. Die Beispielimplementierung von **OnInitDialog** ruft einen Wert aus der Registrierung ab, damit die aktuelle Skalierungsfaktoreinstellung angezeigt werden kann. Die **Beispielimplementierungen** von Apply überprüfen die Benutzereingabe durch Tests, um sicherzustellen, dass sie innerhalb eines angegebenen Bereichs liegen, dann den Wert in der Registrierung beibehalten und dann den Wert (falls gültig) an die Put-Methode der DSP-Plug-In-Eigenschaft mit dem Namen **put \_ scale** übergeben.

Darüber hinaus müssen Sie Code hinzufügen, um das Ereignis zu behandeln, das auftritt, wenn der Benutzer einen Wert in einem Steuerelement ändert, das Sie auf der Eigenschaftenseite angeben. Beispielsweise implementiert der Plug-In-Assistent eine Funktion namens **OnChangeScale,** die einfach die Schaltfläche **Anwenden** aktiviert, wenn der Benutzer den Text im Bearbeitungsfeld auf der Eigenschaftenseite ändert, indem er die **SetDirty-Methode** mit dem Argumentwert **TRUE** aufruft.

## <a name="about-the-property-page-dialog-resource"></a>Informationen zur Dialogfeldressource der Eigenschaftenseite

Die Benutzeroberfläche für die Eigenschaftenseite wird als Dialogressource gespeichert. Sie können das Eigenschaftenseitendialogfeld in Visual Studio anzeigen und bearbeiten, indem Sie im Fenster Project Arbeitsbereich die Registerkarte **ResourceView** auswählen, den Ordner **Dialogfeld** öffnen und dann auf den Ressourcennamen der Eigenschaftenseite doppelklicken. Der Dialogressourcen-Editor in Visual Studio bietet Ihnen die Tools, die Sie zum Hinzufügen von Steuerelementen zum Eigenschaftenseitendialogfeld und zum Erstellen von Ereignishandlern benötigen, die den entsprechenden Windows-Meldungen zugeordnet sind. Ausführliche Informationen zur Verwendung des Ressourcen-Editors in Visual Studio finden Sie in Visual Studio Hilfe.

## <a name="about-ispecifypropertypages"></a>Informationen zu ISpecifyPropertyPages

Wenn ein DSP-Plug-In eine Eigenschaftenseite bereitstellt, muss das Plug-In die **ISpecifyPropertyPages-Schnittstelle** implementieren. Diese Schnittstelle enthält nur eine Methode: **ISpecifyPropertyPages::GetPages**. Dies ist die Methode, mit der die Eigenschaftenseite dem DSP-Plug-In zugeordnet wird. Windows Media Player ruft diese Methode auf, wenn der Benutzer die Eigenschaftenseite aufruft, und übergibt einen Parameter vom Typ CAUUID, bei dem es sich um ein gezähltes Array von GUIDs handelt. Die Beispiel-Plug-In-Implementierung von **GetPages** füllt diese Struktur mit einer einzelnen GUID, die die Klassen-ID des Plug-In-Eigenschaftenseitenobjekts ist. Windows Media Player verwendet dann die Klassen-ID, um das Eigenschaftenseitenobjekt zu erstellen.

Möglicherweise stellen Sie fest, dass in der Beispielimplementierungen von **GetPages** **CoTaskMemAlloc** verwendet wird, um Speicher für die GUID-Struktur zuzuordnen. Es liegt in der Verantwortung des Aufrufers, in diesem Fall Windows Media Player, **CoTaskMemFree** zum Freigeben des Arbeitsspeichers zu verwenden. Ausführliche Informationen zur CAUUID-Struktur finden Sie in der Dokumentation zum Plattform-SDK.

## <a name="about-the-proxystub-dll"></a>Informationen zur Proxy-/Stub-DLL

Damit ein DSP-Plug-In in Windows Media Player 11 funktioniert, das auf Windows Vista ausgeführt wird, müssen Sie eine Proxy-/Stub-DLL für benutzerdefinierte Schnittstellen bereitstellen, die verwendet werden, um Änderungen in den Einstellungen von einem Eigenschaftenseitendialogfeld an die Plug-In-Klasse zu übermitteln. Methodenaufrufe, die über solche Schnittstellen erfolgen, müssen gemarshallt werden, wenn die Aufrufe über Prozess- oder Apartmentgrenzen hinweg erfolgen. Die neueste Version des Plug-In-Assistenten erstellt ein Beispielprojekt für eine Proxy-/Stub-DLL.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Audio-DSP-Plug-Ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




