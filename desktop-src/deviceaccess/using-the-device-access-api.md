---
title: Verwenden der Geräte Zugriffs-API
description: Dieses Thema enthält Aufgaben und Entwurfs Überlegungen für die Verwendung der Geräte Zugriffs-API.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 29c4812c559b691a896fb5bb9da39064bf3c8614
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391182"
---
# <a name="how-to-use-the-device-access-api"></a>Verwenden der Geräte Zugriffs-API

Dieses Thema enthält Aufgaben und Entwurfs Überlegungen für die Verwendung der Geräte Zugriffs-API.

## <a name="steps"></a>Schritte

| Thema | BESCHREIBUNG |
|---|---|
| [Entwurfs Überlegungen für benutzerdefinierte Geräte](design.md)<br/> | In diesem Thema werden Entwurfs Überlegungen beschrieben, mit denen Sie bestimmen können, ob Ihr Gerät einen benutzerdefinierten Treiber benötigt.<br/> |
| [Implementieren des Geräte Zugriffs Objekts](create-the-device-access-object.md)<br/> | In diesem Thema wird erläutert, wie das Geräte Zugriffs Objekt instanziiert und für den Zugriff auf ein Gerät verwendet wird. <br/>  |
| [Deklarieren der Geräte Funktion](declaring-the-device-capability.md)<br/> | In diesem Thema wird erläutert, wie Sie die Geräte Funktions-GUID deklarieren.<br/> |
| [Registrieren der Geräteschnittstelle, wie auf privilegierte apps beschränkt](register-the-device-interface-class-as-privileged.md)<br/> | In diesem Thema wird gezeigt, wie Sie die **Eingeschränkte** Eigenschaft hinzufügen, die angibt, dass nur privilegierte apps auf eine Geräteschnittstellen Klasse zugreifen können.<br/> |
| [Erstellen einer Windows-Runtime Erweiterung](create-a-windows-runtime-extension.md)<br/> | Sie können eine Windows-Runtime Komponente erstellen, um die Komponente zu wrappen, die auf den Treiber zugreift. Anschließend können Sie eine Windows Store-Geräte-App für Ihr Gerät in c# oder JavaScript schreiben.<br/> |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- Das [Beispiel für den benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) veranschaulicht, wie die Geräte Zugriffs-APIs verwendet werden, um über eine Windows Store-Geräte-App auf einen benutzerdefinierten Treiber zuzugreifen
- [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) bietet Ressourcen, um mehr über das Entwerfen und entwickeln von Windows Store-Geräte-Apps für spezialisierte Geräte zu erfahren.
- Das [Hardware dev Center](/windows-hardware/drivers/) bietet allgemeine Ressourcen für Windows Store-Geräte-App-Entwicklungsaufgaben, die für alle Gerätetypen gelten.
