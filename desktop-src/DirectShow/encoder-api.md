---
description: Encoder-API
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: Encoder-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392773"
---
# <a name="encoder-api"></a>Encoder-API

Die Encoder-API bietet eine einheitliche Schnittstelle zum Konfigurieren von Software-und Hardware Encodern. Anwendungen können die Encoder-API verwenden, um einen Encoder zu konfigurieren und die Konfigurationseinstellungen zu speichern. Encoder-Anbieter können die Encoder-API verwenden, um die Funktionen eines Encoders verfügbar zu machen. Obwohl die Encoder-API primär für Encoder entwickelt wurde, ist sie allgemein ausreichend, dass Decoder Sie auch unterstützen können.

Die Encoder-API wird für Anwendungen über die [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle verfügbar gemacht, die durch den Encoder-Filter verfügbar gemacht wird. Der Encoder-Filter kann ein nativer DirectShow-Filter, ein Hardware Encoder oder ein DirectX Media Object (DMO) sein.

-   Software Filter: ein Encoder, der als nativer DirectShow-Filter implementiert ist, sollte [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) direkt verfügbar machen.
-   Hardware Encoder: das Codierungs Gerät wird durch einen oder mehrere AVStream-Mini Treiber bereitgestellt, die im Benutzermodus durch ksproxy dargestellt werden. Ksproxy übersetzt [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Methodenaufrufe in KS-Eigenschaften Sätze. Weitere Informationen finden Sie in der DDK-Dokumentation.
-   DMOS: der DMO sollte die [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle verfügbar machen. DirectShow-Anwendungen können den DMO-Wrapper Filter Abfragen, der die Schnittstelle durch aggregierten DMO verfügbar macht. Anwendungen, die nicht auf DirectShow basieren, können den DMO direkt abfragen.

### <a name="encoder-capabilties"></a>Codierer

Ein Encoder kann eine Liste der Funktionen auf hoher Ebene registrieren, indem er Sie in der Systemregistrierung speichert. Jede Funktion wird durch eine GUID identifiziert. Gehen Sie folgendermaßen vor, um die Funktionen eines bestimmten Encoders aufzulisten:

1.  Erstellen Sie den Moniker, der den encoderfilter darstellt. (Weitere Informationen finden [Sie unter Verwenden des Enumerators für System Geräte](using-the-system-device-enumerator.md).)
2.  Fragen Sie den Filter Moniker für die [**igetcapabilitieskey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) -Schnittstelle ab.
3.  Nennen Sie [**igetcapabilitieskey:: getcapabilitieskey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey). Die-Methode gibt ein Handle für den Registrierungsschlüssel zurück, der die Funktionsliste des Filters enthält.
4.  Um die Werte für den zurückgegebenen Schlüssel aufzulisten, können Sie die Funktion " **RegEnumValue** " aufzählen.

Wenn Sie einen Encoder entwickeln, erstellen Sie die Registrierungseinträge für die Funktionen, wenn der Filter registriert wird. Erstellen Sie bei Software Filtern einen Schlüssel mit dem Namen " **Funktionen** ", der sich neben den Schlüsseln " **FilterData** " und " **FriendlyName** " befindet. Normalerweise würden Sie diese Informationen nach dem Aufrufen von [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) hinzufügen, um die Standardfilter Daten zu registrieren. Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md). Alternativ können Sie einen **capabilitieslocation** -Schlüssel erstellen, der eine Zeichenfolge enthält **, die den** Speicherort des Funktions Schlüssels in der Registrierung enthält. Die Zeichenfolge sollte mit "HKLM \\ ", "HKCR \\ " oder "HKCU" beginnen, \\ um die Registrierungs Unterstruktur anzugeben. Bei Plug & Play Geräten sollten die Setup Dateien des Treibers einen Funktions **Schlüssel erstellen** , der an den Schlüssel " **FriendlyName** " des Filters angrenzt, oder Sie können einen **capabilitieslocation** -Schlüssel verwenden, wie für Softwarefilter beschrieben.

Nachdem **Sie den Funktions** Schlüssel erstellt haben, erstellen Sie einen Wert für jede Funktions-GUID. Der Name des Werts muss die Zeichen folgen Form der GUID im Format sein `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Jeder Werttyp muss einer der folgenden sein:

-   Einzelner numerischer Wert. Verwenden Sie einen **DWORD** -Wert.
-   GUID. Verwenden Sie die Zeichen folgen Form der GUID.
-   Numerische Paare. Verwenden Sie eine Zeichenfolge im Format "a, b", um Wertepaare darzustellen, z. b. Breite und Höhe, oder Zähler und Nenner für Bruchteile.
-   Arrays von-Werten. Verwenden Sie mehrere Zeichen folgen (**reg \_ SZ \_ Multi**), um mehr als einen Wert darzustellen.

Das folgende Beispiel zeigt das Registrierungs Layout für einen Softwarefilter:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Codierprofile

Bei einem *Codierungs Profil* handelt es sich um eine Liste fester Konfigurationseinstellungen, die zur Laufzeit auf einen Encoder angewendet werden können. Profile sind unabhängig vom Encoder. eine Anwendung kann einen Encoder auswählen und dann ein Profil auswählen und die Profileinstellungen auf den Encoder anwenden. Profile werden anhand der GUID identifiziert und sollten an folgendem Speicherort in der Registrierung gespeichert werden:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



*Profil-GUID*

die Zeichen folgen Form der GUID, die das Profil identifiziert. Erstellen Sie Werte für jede Einstellung. Erstellen Sie außerdem einen Zeichen folgen Wert mit dem Namen "FriendlyName", dessen Daten das Profil identifizieren (z. b. "lowbandwidthvideo").

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Encoder-und decoderentwicklung](encoder-and-decoder-development.md)
</dt> </dl>

 

 



