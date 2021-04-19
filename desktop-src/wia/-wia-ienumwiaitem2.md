---
description: Wird von Anwendungen verwendet, um IWiaItem2-Objekte im aktuellen Ordner der Elementstruktur aufzulisten.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: IEnumWiaItem2-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348453"
---
# <a name="ienumwiaitem2-interface"></a>IEnumWiaItem2-Schnittstelle

Wird von Anwendungen verwendet, um [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte im aktuellen Ordner der Elementstruktur aufzulisten.

## <a name="members"></a>Member

Die **IEnumWiaItem2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IEnumWiaItem2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEnumWiaItem2** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](-wia-ienumwiaitem2-clone.md)       | Erstellt eine zusätzliche Instanz der **IEnumWiaItem2** -Schnittstelle und sendet einen Zeiger darauf zurück. <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | Gibt die Anzahl von Elementen zurück, die von diesem Enumerator gespeichert werden. <br/>                                                          |
| [**Weiter**](-wia-ienumwiaitem2-next.md)         | Füllt ein Array von Zeigern auf [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen auf.<br/>                                       |
| [**Zurücksetzen**](-wia-ienumwiaitem2-reset.md)       | Setzt den enumerationsverweis auf das erste [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt zurück. <br/>                          |
| [**Überspringen**](-wia-ienumwiaitem2-skip.md)         | Überspringt die angegebene Anzahl von Elementen während einer Enumeration verfügbarer [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
