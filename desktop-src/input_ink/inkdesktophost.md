---
description: Implementiert die iinkdesktophost-Schnittstelle.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Inkdesktophost-Klasse
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106365221"
---
# <a name="inkdesktophost-class"></a>Inkdesktophost-Klasse

Implementiert die [**iinkdesktophost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) -Schnittstelle.

Ein [**iinkdesktophost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) -Objekt ermöglicht das Übertragen von Eingaben, die Verarbeitung und das Rendering durch die Erstellung eines App-Threads zum Hosten eines [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekts und das Einfügen in die visuelle [directcomposition](../directcomp/directcomposition-portal.md) -Struktur der app.

## <a name="members"></a>Member

Die **inkdesktophost** -Klasse erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inkdesktophost** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inkdesktophost** -Klasse verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
|---|---|
| [**"Kreateandinitializabkpresenter"**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Erstellt ein [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekt in einem Anwendungs Thread, verbindet es mit der visuellen Struktur des [directcomposition](../directcomp/directcomposition-portal.md) -Objekts der APP und legt die Größe des-Objekts fest.<br/> |
| [**"Kreatabkpresenter"**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Erstellt ein [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekt in einem Anwendungs Thread.<br/> |
| [**Queueworkitem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Fügen Sie einer Arbeits Warteschlange einen frei Hand Vorgang zur Ausführung auf dem **inkdesktophost** -Thread hinzu.<br/> |

## <a name="creationaccess-functions"></a>Zugriffs Funktionen für die Erstellung \\

Rufen Sie [<strong>cokreateinstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem Klassen Bezeichner <strong>inkdesktophost</strong> auf, um einen Verweis auf das Objekt abzurufen.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---|---|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/> |
| Header<br/>                   | <dl> <dt>Inkpresenterdesktop. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Inkpresenterdesktop. idl</dt> </dl> |
| IID<br/>                      | IID \_ iinkdesktophost ist als 4ce7d875-A981-4140-a1ff-ad93258e8d59 definiert.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Ink Presenter-Klassen](ink-presenter-classes.md), [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions), Handschrift Analyse- [Beispiel](/samples/microsoft/windows-universal-samples/inkanalysis/), [einfaches Beispiel zum Einfügen](/samples/microsoft/windows-universal-samples/simpleink/), Beispiel für [komplexe](/samples/microsoft/windows-universal-samples/complexink/) Erfassung
