---
title: Verwenden des Gerätezugriffs-API
description: Dieses Thema enthält Aufgaben und Entwurfsüberlegungen für die Verwendung der Gerätezugriffs-API.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: bd1ddf9d2716cd01ab2db8acb08d2793a6831ffa6f20aa2c75378f72932d992b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635300"
---
# <a name="how-to-use-the-device-access-api"></a>Verwenden des Gerätezugriffs-API

Dieses Thema enthält Aufgaben und Entwurfsüberlegungen für die Verwendung der Gerätezugriffs-API.

## <a name="steps"></a>Schritte

| Thema | Beschreibung |
|---|---|
| [Entwurfsüberlegungen für benutzerdefinierte Geräte](design.md)<br/> | In diesem Thema werden Entwurfsüberlegungen beschrieben, mit denen Sie ermitteln können, ob Ihr Gerät einen benutzerdefinierten Treiber benötigt.<br/> |
| [Implementieren des Gerätezugriffsobjekts](create-the-device-access-object.md)<br/> | In diesem Thema wird erläutert, wie Sie das Gerätezugriffsobjekt instanziieren und für den Zugriff auf ein Gerät verwenden. <br/>  |
| [Deklarieren der Gerätefunktion](declaring-the-device-capability.md)<br/> | In diesem Thema wird erläutert, wie Die Gerätefunktions-GUID deklariert wird.<br/> |
| [Registrieren der Geräteschnittstelle als auf privilegierte Apps beschränkt](register-the-device-interface-class-as-privileged.md)<br/> | In diesem Thema wird gezeigt, wie Sie die **Restricted-Eigenschaft** hinzufügen, die angibt, dass nur privilegierte Apps auf eine Geräteschnittstellenklasse zugreifen können.<br/> |
| [Erstellen einer Windows Runtime-Erweiterung](create-a-windows-runtime-extension.md)<br/> | Sie können eine Komponente Windows Runtime erstellen, um die Komponente zu umschließen, die auf Ihren Treiber zutritt. Anschließend können Sie eine Windows Store-App für Ihr Gerät in C# oder JavaScript schreiben.<br/> |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- Im [Beispiel für den benutzerdefinierten Treiberzugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) wird veranschaulicht, wie Sie die Gerätezugriffs-APIs verwenden, um über eine gerätespezifische Windows Store auf einen benutzerdefinierten Treiber zu zugreifen.
- [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) bieten Ressourcen, um mehr über das Entwerfen und Entwickeln Windows Store Geräte-Apps für spezialisierte Geräte zu erfahren.
- Der [Hardware Dev Center](/windows-hardware/drivers/) stellt allgemeine Ressourcen für Windows Store Entwicklungsaufgaben für Geräte-Apps zur Verfügung, die für alle Gerätetypen gelten.
