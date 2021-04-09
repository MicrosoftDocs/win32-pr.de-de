---
description: Die IWiaDevMgr2-Schnittstelle wird verwendet, um Abbild Erfassungsgeräte zu erstellen und zu verwalten sowie zum Empfangen von Geräte Ereignissen zu registrieren.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: IWiaDevMgr2-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865247"
---
# <a name="iwiadevmgr2-interface"></a>IWiaDevMgr2-Schnittstelle

Die **IWiaDevMgr2** -Schnittstelle wird verwendet, um Abbild Erfassungsgeräte zu erstellen und zu verwalten sowie zum Empfangen von Geräte Ereignissen zu registrieren.

## <a name="members"></a>Member

Die **IWiaDevMgr2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IWiaDevMgr2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaDevMgr2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatedevice"**](-wia-iwiadevmgr2-createdevice.md)                                     | Erstellt eine hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten für ein WIA 2,0-Gerät. <br/>                                                                                                                                                                                                                                                                                                 |
| [**Enumdäviceingefo**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | Erstellt einen Enumerator mit Eigenschafts Informationen für jedes verfügbare WIA 2,0-Gerät. <br/>                                                                                                                                                                                                                                                                                                                 |
| [**Getimagedlg**](-wia-iwiadevmgr2-getimagedlg.md)                                       | Die [**IWiaDevMgr2:: getimagedlg**](-wia-iwiadevmgr2-getimagedlg.md) -Methode zeigt ein oder mehrere Dialogfelder an, mit denen ein Benutzer ein Bild von einem WIA 2,0-Gerät abrufen und in eine angegebene Datei schreiben kann. Mit dieser Methode wird die Funktionalität von [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) erweitert, um die Bild Erfassung innerhalb eines einzelnen API-Aufrufs zu kapseln. <br/> |
| [**Registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | Mit der [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md) -Methode wird eine Anwendung zum Empfangen von Ereignissen registriert, auch wenn die Anwendung nicht ausgeführt wird.<br/>                                                                                                                                                                                                      |
| [**Registereventcallbackinterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) | Registriert eine laufende Anwendung für die WIA 2,0-Ereignis Benachrichtigung. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**Registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | Die [**IWiaDevMgr2:: registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) -Methode registriert eine Anwendung, um Geräte Ereignisse zu empfangen. Es wird hauptsächlich aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für WIA 2,0 geschrieben wurden.<br/>                                                                                                                         |
| [**Selectde vicedlg**](-wia-iwiadevmgr2-selectdevicedlg.md)                               | Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann. <br/>                                                                                                                                                                                                                                                                                                   |
| [**Selectdebug-lgid**](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann. <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Die **IWiaDevMgr2** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
