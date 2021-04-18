---
title: Neuerungen in Windows Vista
description: Version 1,0 der Abbild Farbverwaltung (Image Color Management, ICM) wurde in Microsoft Windows 95 bereitgestellt und stellt grundlegende Farb Verwaltungsfunktionen innerhalb von Windows-Geräte Kontexten bereit.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS), Windows Vista
- WCS (Windows Color System), Windows Vista
- Bildfarben Verwaltung, Windows Vista
- Farbverwaltung, Windows Vista
- Farben, Windows Vista
- Windows Color System (WCS), Betriebssysteme
- WCS (Windows Color System), Betriebssysteme
- Abbild Farben Verwaltung, Betriebssysteme
- Farbverwaltung, Betriebssysteme
- Farben, Betriebssysteme
- Farbverwaltung (Image Color Management; ICM)
- ICM (Bildfarben Verwaltung)
- Windows Vista-Farbverwaltung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106354887"
---
# <a name="whats-new-in-windows-vista"></a>Neuerungen in Windows Vista

Version 1,0 der Abbild Farbverwaltung (Image Color Management, ICM) wurde in Microsoft Windows 95 bereitgestellt und stellt grundlegende Farb Verwaltungsfunktionen innerhalb von Windows-Geräte Kontexten bereit.

Die ICM-Version 2,0 wurde in Windows 98, Windows Millennium Edition, Windows 2000 und Windows XP bereitgestellt und enthielt eine Reihe von neuen Funktionen, die die Farbverwaltung außerhalb der Geräte Kontexte implementierten. Diese neuen Funktionen waren für anspruchsvollere Anforderungen an die Farbverwaltung geeignet und lieferten Anwendungen eine bessere Kontrolle über den Farb Verwaltungsprozess.

Mit der Veröffentlichung von Windows Vista ist ICM 2,0 jetzt in Windows Color System (WCS) 1,0 enthalten. Dadurch werden weitere Funktionen hinzugefügt. In der folgenden Tabelle werden neue Anwendungs Programmierschnittstellen (API) aufgelistet, die in Windows Vista ausgeliefert werden.

## <a name="new-api-shipping-in-windows-vista"></a>Neuer API-Versand in Windows Vista



Enumerationen

API-Name

Header

Bibliothek

[**Colordatatype**](/windows/win32/api/icm/ne-icm-colordatatype)

ICM. h

mscms. lib

[**Colorprofilesubtype**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

ICM. h

mscms. lib

[**Colorprofiletype**](/windows/win32/api/icm/ne-icm-colorprofiletype)

ICM. h

mscms. lib

[**WCS- \_ Profil \_ Verwaltungs \_ Bereich**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

ICM. h

mscms. lib



 



Functions

API-Name

Header

Bibliothek

[**Wcsassociatecolorprofilewithdevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

mscms. lib

[**Wcscheckcolors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

mscms. lib

[**Wcscreateiccprofile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

ICM. h

mscms. lib

[**Wcsdisassociatecolorprofilefromdevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

ICM. h

mscms. lib

[**Wcsenaufcolorprofiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

ICM. h

mscms. lib

[**Wcsenaufcolorprofilessize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

ICM. h

mscms. lib

[**Wcsgetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

ICM. h

mscms. lib

[**Wcsgetdefaultcolorprofilesize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

ICM. h

mscms. lib

[**Wcsgetdefaultrenderingintent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

mscms. lib

[**Wcsgetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

mscms. lib

[**Wcsopeincolorprofilew**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

ICM. h

mscms. lib

[**Wcssetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

ICM. h

mscms. lib

[**Wcssetdefaultrenderingintent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

ICM. h

mscms. lib

[**Wcssetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

ICM. h

mscms. lib

[**Wcstranslatecolors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

ICM. h

mscms. lib



 



Schnittstellen und ihre Funktionen

API-Name

Header

Bibliothek

[**Idevicemodelplugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

Wcsplugin. h

–

[**Idevicemodelplugin:: colormetrictodevicecolors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

Wcsplugin. h

–

[**Idevicemodelplugin:: colormetrictodevicecolorswithblack**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

Wcsplugin. h

–

[**Idevicemodelplugin::D evicetocolormetriccolors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

Wcsplugin. h

–

[**Idevicemodelplugin:: getgamutboundarymesh**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

Wcsplugin. h

–

[**Idevicemodelplugin:: getgamutboundarymeschsize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

Wcsplugin. h

–

[**Idevicemodelplugin:: getneutralaxis**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

Wcsplugin. h

–

[**Idevicemodelplugin:: getneutralaxissize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

Wcsplugin. h

–

[**Idevicemodelplugin:: getnumchannels**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

Wcsplugin. h

–

[**Idevicemodelplugin:: getprimarysamples**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

Wcsplugin. h

–

[**Idevicemodelplugin:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

Wcsplugin. h

–

[**Idevicemodelplugin:: settransformdevicemodelinfo**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

Wcsplugin. h

–

[**Igamutmapmodelplugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

Wcsplugin. h

–

[**Igamutmapmodelplugin:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

Wcsplugin. h

–

[**Igamutmapmodelplugin:: sourceesdestinationdestinancecolors**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

Wcsplugin. h

–



 



Strukturen

API-Name

Header

Bibliothek

[**Blackinformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

Wcsplugin. h

–

[**Gamutboundarydescription**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

Wcsplugin. h

–

[**Xyzcolorf**](https://www.bing.com/search?q=**XYZColorF**)

Wcsplugin. h

–

[**Jchcolorf**](https://www.bing.com/search?q=**JChColorF**)

Wcsplugin. h

–

[**Jabcolorf**](https://www.bing.com/search?q=**JabColorF**)

Wcsplugin. h

–

[**Gamutshell**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

Wcsplugin. h

–

[**Gamutshelldreieck**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

Wcsplugin. h

–

[**Primaryjabcolors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

Wcsplugin. h

–

[**Primaryxyzcolors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

Wcsplugin. h

Nicht zutreffend



 

 

 