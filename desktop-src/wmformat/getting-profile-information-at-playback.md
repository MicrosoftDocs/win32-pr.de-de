---
title: Erhalten von Profilinformationen bei der Wiedergabe
description: Erhalten von Profilinformationen bei der Wiedergabe
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media-Format-SDK, profile
- Advanced Systems Format (ASF), profile
- ASF (Advanced Systems Format), profile
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- Advanced Systems Format (ASF), Bandbreiten Freigabe
- ASF (Advanced Systems Format), Bandbreiten Freigabe
- Streams, erhalten von Profilinformationen bei der Wiedergabe
- Profile, erhalten von Informationen bei der Wiedergabe
- gegenseitiger Ausschluss, erhalten von Profilinformationen bei der Wiedergabe
- Bandbreiten Freigabe, erhalten von Profilinformationen bei der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101278"
---
# <a name="getting-profile-information-at-playback"></a>Erhalten von Profilinformationen bei der Wiedergabe

Informationen aus dem Profil, das zum Erstellen einer Datei verwendet wird, werden im Header Abschnitt der Datei gespeichert. Beide Reader-Objekte können über den Dateiheader auf die Profilinformationen zugreifen. Es gibt mehrere Gründe, warum Sie auf die Profildaten des Readers zugreifen können. In den meisten Fällen müssen Sie Informationen zu Streams, gegenseitigen Ausschluss Objekten und Bandbreiten Freigabe Objekten abrufen.

Sowohl das asynchrone Reader-Objekt als auch das synchrone Reader-Objekt können für die [**iwmprofile**](iwmprofile.md) -Schnittstelle abgefragt werden. Keine Änderungen an den Profilinformationen können Auswirkungen auf die Datei im Reader haben. Weitere Informationen zum Zugreifen auf Profilinformationen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).

## <a name="stream-information"></a>Streaminformationen

Manchmal ist es wichtig zu wissen, wie ein Stream konfiguriert wird. Wenn Sie Medien Eigenschaften von einem der Reader-Objekte abrufen, werden die Eigenschaften der Ausgaben abgerufen. Ausgabe Eigenschaften beschreiben, wie die unkomprimierten Daten aus einem Stream vom Reader übermittelt werden, nicht wie der Stream innerhalb der ASF-Datei konfiguriert wird.

Wenn Sie nicht komprimierte streambeispiele von einem der Reader-Objekte empfangen, müssen Sie die Profilinformationen verwenden, um das Format der komprimierten Daten zu identifizieren. Dies ist besonders wichtig, wenn Sie den komprimierten Stream in eine andere ASF-Datei schreiben möchten.

Sie müssen auch auf streaminformationen zugreifen, wenn Sie eine intelligente Neukomprimierung verwenden, um einen Audiostream in eine niedrigere Bitrate zu transcodieren.

Möglicherweise möchten Sie ermitteln, ob ein Datenstrom mithilfe von VBR-Codierung (Variable Bitrate) geschrieben wurde. Es ist nicht möglich, auf VBR-Informationen von der **iwmprofile** -Schnittstelle eines Reader-Objekts zuzugreifen. Dies liegt daran, dass die VBR-Informationen nach der Codierung nicht in der Datei gespeichert werden. Sie können mithilfe der VBR-Codierung ermitteln, ob ein Stream erstellt wurde, indem Sie einen Zeiger auf die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle des Reader-Objekts erhalten und [**iwmheaderinfo:: getattributebyname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)aufrufen. Sie müssen die Datenstrom Nummer angeben und g \_ wszisvbr als Attributnamen übergeben.

## <a name="mutual-exclusion-information"></a>Informationen zum gegenseitigen Ausschluss

Wenn Sie eine Leseanwendung erstellen möchten, die den gegenseitigen Ausschluss verwendet, sollten Sie auf die Informationen zu allen gegenseitigen Ausschluss Objekten im Profil zugreifen. Für alle gegenseitigen Ausschluss Typen außer der Bitrate ist die Leseanwendung für jeden erforderlichen Datenstrom Wechsel verantwortlich. Um Streams zu wechseln, müssen Sie wissen, welche Streams welche Datenströme haben.

## <a name="bandwidth-sharing-information"></a>Informationen zur Bandbreiten Freigabe

Bandbreiten Freigabe Objekte, die in einem Profil enthalten sind, sind nur zu Informationszwecken enthalten. Weder das Writer-Objekt noch eines der Reader-Objekte führt eine Aktion aus, die durch die Bandbreiten Freigabe von Daten verursacht wird. Wenn Sie die Bandbreiten Freigabe in der Leseanwendung verwenden möchten, müssen Sie auf die Informationen zur Bandbreiten Freigabe aus den Profildaten zugreifen.

> [!Note]  
> Nicht alle Informationen aus dem Profil, das zum Erstellen einer Datei verwendet wird, sind im Dateiheader vorhanden. Als allgemeine Regel werden Daten, die nur zum Zeitpunkt der Codierung verwendet werden, nicht in der Datei gespeichert. Dies schließt Eingabeeinstellungen ein, die mithilfe der [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) -Methode festgelegt wurden, sowie Eigenschaften, die mithilfe der [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) -Methode festgelegt wurden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmprofile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




