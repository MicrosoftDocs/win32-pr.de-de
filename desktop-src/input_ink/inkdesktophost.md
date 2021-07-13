---
description: Implementiert die IInkDesktopHost-Schnittstelle.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: InkDesktopHost-Klasse
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
ms.openlocfilehash: 74eebdbdfdbe3a4018d63b1f2161687152ebb5cc
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689223"
---
# <a name="inkdesktophost-class"></a>InkDesktopHost-Klasse

Implementiert die [**IInkDesktopHost-Schnittstelle.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)

Ein [**IInkDesktopHost-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) ermöglicht das Eingeben, Verarbeiten und Rendern von Freihandeingaben durch die Erstellung eines App-Threads, um ein [**IInkPresenterDesktop-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) zu hosten und in die visuelle [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der App einzufügen.

## <a name="members"></a>Member

Die **InkDesktopHost-Klasse** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **InkDesktopHost** verfügt auch über diese Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **InkDesktopHost-Klasse** verfügt über diese Methoden.

| Methode | Beschreibung |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Erstellt ein [**IInkPresenterDesktop-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in einem Anwendungsthread, verbindet es mit der visuellen [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der App und legt die Größe des Objekts fest.<br/> |
| [**CreateInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Erstellt ein [**IInkPresenterDesktop-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in einem Anwendungsthread.<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Fügen Sie einer Arbeitswarteschlange einen Inkk-Vorgang für die Ausführung im **InkDesktopHost-Thread** hinzu.<br/> |

## <a name="creationaccess-functions"></a>\\Erstellungszugriffsfunktionen

Rufen Sie [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem Klassenbezeichner <strong>InkDesktopHost</strong> auf, um einen Verweis auf das Objekt abzurufen.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---|---|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/> |
| Header<br/>                   | <dl> <dt>InkPresenterDesktop.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>InkPresenterDesktop.idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkDesktopHost ist als 4ce7d875-a981-4140-a1ff-ad93258e8d59 definiert.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Klassen für die Ink-Präsentation,](ink-presenter-classes.md) [Stift- und Stiftinteraktionen,](/windows/uwp/design/input/pen-and-stylus-interactions) [Beispiel für die Ink-Analyse,](/samples/microsoft/windows-universal-samples/inkanalysis/) [Einfaches Beispiel für Denkaktionen,](/samples/microsoft/windows-universal-samples/simpleink/)Beispiel für [komplexes Inknen](/samples/microsoft/windows-universal-samples/complexink/)
