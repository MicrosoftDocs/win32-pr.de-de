---
title: Abrufen von Profilinformationen bei der Wiedergabe
description: Abrufen von Profilinformationen bei der Wiedergabe
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Medienformat-SDK, Profile
- Advanced Systems Format (ASF),profiles
- ASF (Advanced Systems Format), Profiles
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- Advanced Systems Format (ASF), Bandbreitenfreigabe
- ASF (Advanced Systems Format), Bandbreitenfreigabe
- Streams,Abrufen von Profilinformationen bei der Wiedergabe
- Profile,Abrufen von Informationen bei der Wiedergabe
- Gegenseitiger Ausschluss, Abrufen von Profilinformationen bei der Wiedergabe
- Bandbreitenfreigabe,Abrufen von Profilinformationen bei der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0f9386301b426adb3c4c425ac9329309c7e45146e312cc41df0bd1c453d485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839920"
---
# <a name="getting-profile-information-at-playback"></a>Abrufen von Profilinformationen bei der Wiedergabe

Informationen aus dem Profil, das zum Erstellen einer Datei verwendet wird, werden im Headerabschnitt der Datei gespeichert. Beide Readerobjekte können über den Dateiheader auf die Profilinformationen zugreifen. Es gibt mehrere Gründe, warum Sie vom Leser aus auf Profildaten zugreifen möchten. In den meisten Jahren müssen Sie Informationen zu Streams, gegenseitigen Ausschlussobjekten und Bandbreitenfreigabeobjekten abrufen.

Sowohl das asynchrone Readerobjekt als auch das synchrone Readerobjekt können für die [**IWMProfile-Schnittstelle abgefragt**](iwmprofile.md) werden. Keine Änderungen an den Profilinformationen können Auswirkungen auf die Datei im Reader haben. Weitere Informationen zum Zugreifen auf Profilinformationen finden Sie unter [Arbeiten mit Profilen.](working-with-profiles.md)

## <a name="stream-information"></a>Streamen von Informationen

Manchmal ist es wichtig zu wissen, wie ein Stream konfiguriert ist. Wenn Sie Medieneigenschaften aus einem der Readerobjekte abrufen, erhalten Sie die Eigenschaften der Ausgaben. Ausgabeeigenschaften beschreiben, wie die unkomprimierten Daten aus einem Stream vom Reader übermittelt werden, nicht wie der Stream in der ASF-Datei konfiguriert wird.

Wenn Sie nicht komprimierte Streambeispiele von beiden Readerobjekten empfangen, müssen Sie die Profilinformationen verwenden, um das Format der komprimierten Daten zu identifizieren. Dies ist besonders wichtig, wenn Sie den komprimierten Stream in eine andere ASF-Datei schreiben möchten.

Sie müssen auch auf Streaminformationen zugreifen, wenn Sie die intelligente Rekomprimierung verwenden, um einen Audiodatenstrom mit einer niedrigeren Bitrate zu transcodieren.

Möglicherweise möchten Sie ermitteln, ob ein Stream mit VBR-Codierung (Variable Bit Rate) geschrieben wurde. Sie können nicht über die **IWMProfile-Schnittstelle** eines der Reader-Objekte auf VBR-Informationen zugreifen. Dies liegt daran, dass die VBR-Informationen nach der Codierung nicht in der Datei gespeichert werden. Sie können bestimmen, ob ein Stream mit VBR-Codierung erstellt wurde, indem Sie einen Zeiger auf die [**IWMHeaderInfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) des Readerobjekts abrufen und [**IWMHeaderInfo::GetAttributeByName aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname) Sie müssen die Streamnummer angeben und g \_ wszIsVBR als Attributnamen übergeben.

## <a name="mutual-exclusion-information"></a>Informationen zum gegenseitigen Ausschluss

Wenn Sie eine Leseanwendung erstellen möchten, die gegenseitigen Ausschluss verwendet, sollten Sie auf die Informationen zu allen objekten für gegenseitigen Ausschluss zugreifen, die im Profil enthalten sind. Für alle gegenseitigen Ausschlusstypen mit Ausnahme der Bitrate ist die Leseanwendung für alle erforderlichen Datenstromwechsel verantwortlich. Um Datenströme zu wechseln, müssen Sie wissen, welche Streams welche sind.

## <a name="bandwidth-sharing-information"></a>Informationen zur Bandbreitenfreigabe

Objekte zur Bandbreitenfreigabe, die in einem Profil enthalten sind, sind nur zu Informationszwecken enthalten. Weder das Writerobjekt noch eines der Readerobjekte führt eine Aktion als Ergebnis der Bandbreitenfreigabedaten aus. Wenn Sie die Bandbreitenfreigabe in Ihrer Leseanwendung verwenden möchten, müssen Sie auf die Informationen zur Bandbreitenfreigabe aus den Profildaten zugreifen.

> [!Note]  
> Nicht alle Informationen aus dem Profil, die zum Erstellen einer Datei verwendet werden, sind im Dateiheader vorhanden. Im Allgemeinen werden Daten, die nur zum Zeitpunkt der Codierung verwendet werden, nicht in der Datei beibehalten. Dies schließt Eingabeeinstellungen ein, die mit der [**IWMWriterAdvanced2::SetInputSetting-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) festgelegt wurden, sowie Eigenschaften, die mit der [**IWMPropertyVault::SetProperty-Methode festgelegt**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) wurden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMProfile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




