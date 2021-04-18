---
title: Geräte Registrierungs Objekt
description: Geräte Registrierungs Objekt
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media-Format-SDK, Geräte Registrierungs Objekte
- Advanced Systems Format (ASF), Geräte Registrierungs Objekte
- ASF (Advanced Systems Format), Geräte Registrierungs Objekte
- Objekte, Geräte Registrierungs Objekte
- Geräte Registrierungs Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337634"
---
# <a name="device-registration-object"></a>Geräte Registrierungs Objekt

Mit dem Geräte Registrierungs Objekt wird die Geräte Registrierungsdatenbank verwaltet. In dieser Datenbank werden Informationen zu Netzwerkgeräten, wie z. b. Set-Top-Video Playern, gespeichert, die mit dem Client Computer verbunden sind. Der primäre Zweck der Geräte Registrierungsdatenbank ist die Verwaltung von Geräten, von denen das Windows Media DRM 10 for Network Devices-Protokoll verwendet wird, um gesicherte Datenströme zu empfangen.

Wenn Ihre Anwendung Windows Media DRM 10 für Netzwerkgeräte unterstützt, müssen Sie die Schnittstellen dieses Objekts verwenden, um Netzwerkgeräte zu registrieren und diese Geräte zu überprüfen. Sie können die Geräte Registrierungsdatenbank auch zum Speichern von Informationen zu Netzwerkgeräten verwenden, die nicht Windows Media DRM 10 für Netzwerkgeräte verwenden, obwohl nicht alle Informationen in der-Datenbank auf solche Geräte angewendet werden.

Das Geräte Registrierungs Objekt wird von der [**wmkreatedeviceregistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) -Funktion erstellt, mit der ein Zeiger auf eine **iwmdeviceregistration** -Schnittstelle festgelegt wird. Die anderen Methoden des Geräte Registrierungs Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Geräte Registrierungs Objekt unterstützt.



| Schnittstelle                                              | BESCHREIBUNG                               |
|--------------------------------------------------------|-------------------------------------------|
| [**Iwmdeviceregistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Verwaltet die Geräte Registrierungsdatenbank. |
| [**Iwmdrmmessageparser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analysiert Nachrichten, die von Geräten gesendet werden.          |
| [**Iwmproximityerkennung**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Verwaltet die Gerätevalidierung.                |



 

Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, damit die-Methoden der **iwmproximityerkennungs** -Schnittstelle verwendet werden können.



| Schnittstelle                                      | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**Iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> </dl>

 

 




