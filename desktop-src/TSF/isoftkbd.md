---
title: ISOFT kbd-Schnittstelle (Software-BDC. h)
description: Die isoftkbd-Schnittstelle wird von Anwendungen und Text Diensten verwendet, um eine weiche Tastatur zu implementieren.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Iweichkbd Interface Text Services-Framework
- ISOFT kbd Interface Text Services-Framework, beschrieben
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339309"
---
# <a name="isoftkbd-interface"></a>ISOFT kbd-Schnittstelle

Die **isoftkbd** -Schnittstelle wird von Anwendungen und Text Diensten verwendet, um eine weiche Tastatur zu implementieren.

## <a name="members"></a>Member

Die **iSOFT kbd** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ISOFT kbd** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iSOFT kbd** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                        | BESCHREIBUNG                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Advisesoftkeyboarabventsink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | Installiert eine weiche Tastaturereignis Senke, um onkeyselection-Benachrichtigungen von der Soft Tastatur zu verarbeiten.<br/> |
| [**"Kreatesoftkeyboardlayoutfromresource"**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | Erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.<br/>                                        |
| [**"Kreatesoftkeyboardlayoutfromxmlfile"**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | Erstellt ein weiches Tastaturlayout aus der angegebenen XML-Datei.<br/>                                        |
| [**"Kreatesoftkeyboardwindow"**](isoftkbd-createsoftkeyboardwindow.md)                         | Erstellt ein weiches Tastatur Fenster.<br/>                                                                    |
| [**Destroysoftware keyboardwindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | Zerstört ein weiches Tastatur Fenster.<br/>                                                                   |
| [**Enumsoft Keyboard**](isoftkbd-enumsoftkeyboard.md)                                         | Listet die möglichen weichen Tastaturen auf, die die angegebene Sprache unterstützen.<br/>                        |
| [**Getsoft keyboardcolors**](isoftkbd-getsoftkeyboardcolors.md)                               | Ruft die weiche Tastatur Farbe ab, die dem angegebenen Farbtyp entspricht.<br/>                        |
| [**Getsoft keyboardpossize**](isoftkbd-getsoftkeyboardpossize.md)                             | Ruft die Anfangsposition und die Größe einer Soft Tastatur ab.<br/>                                       |
| [**Getsoftware keyboardtextfont**](isoftkbd-getsoftkeyboardtextfont.md)                           | Ruft die von einer Soft Tastatur verwendete Text Schriftart ab.<br/>                                                   |
| [**Getsoft keyboardtypemode**](isoftkbd-getsoftkeyboardtypemode.md)                           | Ruft den typmodus für eine weiche Tastatur ab.<br/>                                                       |
| [**Initialisieren**](isoftkbd-initialize.md)                                                     | Initialisiert alle erforderlichen Felder für eine weiche Tastatur und generiert standardmäßige weiche Tastaturlayouts.<br/> |
| [**Selectsoft Keyboard**](isoftkbd-selectsoftkeyboard.md)                                     | Wählt die angegebene weiche Tastatur aus.<br/>                                                               |
| [**Setkeyboardlabeltext**](isoftkbd-setkeyboardlabeltext.md)                                 | Legt den Beschriftungs Text aus dem Layout für eine weiche Tastatur fest.<br/>                                           |
| [**Setkeyboardlabeltextkombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | Legt eine Kombination aus Bezeichnung und Text fest, mit der eine weiche Tastatur beschrieben wird.<br/>                             |
| [**Setsoft keyboardcolors**](isoftkbd-setsoftkeyboardcolors.md)                               | Legt die weiche Tastatur Farbe fest, die dem angegebenen Farbtyp entspricht.<br/>                             |
| [**Setsoft keyboardpossize**](isoftkbd-setsoftkeyboardpossize.md)                             | Legt die Anfangsposition und die Größe einer Soft Tastatur fest.<br/>                                            |
| [**Setsoft keyboardtextfont**](isoftkbd-setsoftkeyboardtextfont.md)                           | Legt die von einer Soft Tastatur verwendete Text Schriftart fest.<br/>                                                        |
| [**Setsoft keyboardtypemode**](isoftkbd-setsoftkeyboardtypemode.md)                           | Legt den typmodus für eine weiche Tastatur fest.<br/>                                                            |
| [**Showkeysforkeyscanmode**](isoftkbd-showkeysforkeyscanmode.md)                             | Zeigt die Schlüssel an, die für den Schlüssel Scan Modus für eine weiche Tastatur verwendet werden.<br/>                                  |
| [**ShowSoft Keyboard**](isoftkbd-showsoftkeyboard.md)                                         | Zeigt eine weiche Tastatur an.<br/>                                                                          |
| [**Unadvisesoftkeyboarabventsink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | Entfernt eine weiche Tastaturereignis Senke.<br/>                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Software-Domänen Controller. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Software. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 

