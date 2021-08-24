---
description: Encoder-API
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: Encoder-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b97dc2242cc718605a851186c726e3301493b7637b94e88b7987868741874a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823640"
---
# <a name="encoder-api"></a>Encoder-API

Die Encoder-API bietet eine einheitliche Schnittstelle zum Konfigurieren von Software- und Hardwareencodern. Anwendungen können die Encoder-API verwenden, um einen Encoder zu konfigurieren und die Konfigurationseinstellungen zu speichern. Encoderanbieter können die Encoder-API verwenden, um die Funktionen eines Encoders verfügbar zu machen. Obwohl die Encoder-API in erster Linie für Encoder konzipiert ist, ist sie allgemein genug, dass Decoder sie auch unterstützen können.

Die Encoder-API wird für Anwendungen über die [**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) verfügbar gemacht, die vom Encoderfilter verfügbar gemacht wird. Der Encoderfilter kann ein nativer DirectShow-Filter, ein Hardwareencoder oder ein DirectX-Medienobjekt (DMO) sein.

-   Softwarefilter: Ein Encoder, der als nativer DirectShow-Filter implementiert ist, sollte die [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) direkt verfügbar machen.
-   Hardwareencoder: Das Codierungsgerät wird über einen oder mehrere AVStream-Minitreiber verfügbar gemacht, die durch KSProxy im Benutzermodus dargestellt werden. KSProxy übersetzt [**ICodecAPI-Methodenaufrufe**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) in KS-Eigenschaftensätze. Weitere Informationen finden Sie in der DDK-Dokumentation.
-   DMOs: Die DMO sollte die [**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) verfügbar machen. DirectShow-Anwendungen können den DMO Wrapperfilter abfragen, der die Schnittstelle durch Aggregieren der DMO verfügbar macht. Anwendungen, die nicht auf DirectShow basieren, können die DMO direkt abfragen.

### <a name="encoder-capabilties"></a>Encoder-Capabilties

Ein Encoder kann eine Liste der funktionen auf hoher Ebene registrieren, indem er sie in der Systemregistrierung speichert. Jede Funktion wird durch eine GUID identifiziert. Gehen Sie wie folgt vor, um die Funktionen eines bestimmten Encoders aufzuzählen:

1.  Erstellen Sie den Moniker, der den Encoderfilter darstellt. (Siehe [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).)
2.  Fragen Sie den Filtermoniker für die [**IGetCapabilitiesKey-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) ab.
3.  Rufen Sie [**IGetCapabilitiesKey::GetCapabilitiesKey auf.**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey) Die -Methode gibt ein Handle für den Registrierungsschlüssel zurück, der die Liste der Funktionen des Filters enthält.
4.  Rufen Sie die **RegEnumValue-Funktion** auf, um die Werte für den zurückgegebenen Schlüssel aufzuzählen.

Wenn Sie einen Encoder entwickeln, erstellen Sie die Registrierungseinträge für die Funktionen, wenn der Filter registriert wird. Erstellen Sie für Softwarefilter einen Schlüssel mit dem Namen **Capabilities,** der sich neben den **Schlüsseln FilterData** und **FriendlyName** befindet. In der Regel fügen Sie diese Informationen nach dem Aufruf von [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) hinzu, um die Standardfilterdaten zu registrieren. Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md) Alternativ können Sie einen **CapabilitiesLocation-Schlüssel** erstellen, der eine Zeichenfolge enthält, die den Speicherort des **Capabilities-Schlüssels** in der Registrierung angibt. Die Zeichenfolge sollte mit \\ "HKLM", "HKCR" \\ oder "HKCU" beginnen, \\ um die Registrierungsunterstruktur anzugeben. For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.

Nachdem Sie den **Schlüssel Funktionen** erstellt haben, erstellen Sie einen Wert für jede Funktions-GUID. Der Name des Werts sollte die Zeichenfolgenform der GUID im Format `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` sein. Jeder Werttyp sollte einen der folgenden Werte aufweisen:

-   Einzelner numerischer Wert. Verwenden Sie einen **DWORD-Wert.**
-   GUID. Verwenden Sie die Zeichenfolgenform der GUID.
-   Numerische Paare. Verwenden Sie eine Zeichenfolge mit dem Format "a,b", um Wertepaare wie Breite und Höhe oder Zähler und Nenner für Bruchzahlen darzustellen.
-   Arrays von Werten. Verwenden Sie mehrere Zeichenfolgen (**REG \_ SZ \_ MULTI**), um mehr als einen Wert darzustellen.

Das folgende Beispiel zeigt das Registrierungslayout für einen Softwarefilter:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Encoderprofile

Ein *Encoderprofil* ist eine feste Liste von Konfigurationseinstellungen, die zur Laufzeit auf einen Encoder angewendet werden können. Profile sind unabhängig vom Encoder. Eine Anwendung kann einen Encoder auswählen, dann ein Profil auswählen und die Profileinstellungen auf den Encoder anwenden. Profile werden durch GUID identifiziert und sollten an folgendem Speicherort in der Registrierung gespeichert werden:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



where *Profile GUID*

ist die Zeichenfolgenform der GUID, die das Profil identifiziert. Erstellen Sie Werte für jede Einstellung. Erstellen Sie außerdem einen Zeichenfolgenwert mit dem Namen "FriendlyName", dessen Daten das Profil identifizieren (z. B. "LowBandwidthVideo").

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Encoder- und Decoderentwicklung](encoder-and-decoder-development.md)
</dt> </dl>

 

 



