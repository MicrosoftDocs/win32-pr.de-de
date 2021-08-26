---
description: Ein Telefongerät kann über mehrere Hookswitch-Geräte verfügen.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Hookswitch-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ca5c9f605731780068b9ad5a5b35d913213006c62d127e6a3b15d1ffc5fe1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013100"
---
# <a name="hookswitch-devices"></a>Hookswitch-Geräte

Ein Telefongerät kann über mehrere Hookswitch-Geräte verfügen. Ein Hookschalter ist der Switch, der ein Gerät von der Telefonleitung verbindet oder trennt. Bei einem Telefon ist dies z. B. der Schalter, der automatisch aktiviert wird, wenn ein Benutzer den Empfänger aus der Taste hebt, um einen neuen Wählton zu erhalten. TAPI definiert drei Arten von Hookswitch-Geräten für ein Smartphone: Mobiltelefon, Lautsprecher und Headset. Jedes Hookswitchgerät verfügt über einen Lautsprecher und eine Mikrofonkomponente und arbeitet in einem von vier Hookswitchmodi:

-   **Onhook** Das Hookswitch-Gerät ist onhook, und sowohl das Mikrofon als auch der Lautsprecher sind deaktiviert.
-   **Nur Mikrofon** Das Hookswitchgerät ist offhook, das Mikrofon ist aktiviert, und der Lautsprecher ist stumm.
-   **Nur Sprecher** Das Hookswitchgerät ist offhook, das Mikrofon ist stumm, und der Lautsprecher ist aktiviert.
-   **Mikrofon und Lautsprecher** Das Hookswitch-Gerät ist offhook, und mikrofon und speaker sind aktiviert.

Die [**phoneSetHookSwitch-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) wird verwendet, um den Hookswitchmodus eines oder mehrere hookswitch-Geräte eines offenen Telefongeräts zu aktivieren. Verwenden Sie beispielsweise **phoneSetHookSwitch** mit dem entsprechenden Hookswitch-Modus, um das Mikrofon oder die Lautsprecherkomponente eines Hookswitch-Geräts zu stummschalten oder zu entmutigen. Die [**phoneGetHookSwitch-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) kann verwendet werden, um den Hookswitch-Modus eines Hookswitch-Geräts eines offenen Telefongeräts abfragt.

Wenn der Modus des Hookswitchgeräts eines Telefons manuell geändert wird, z. B. durch Heben des Handsets aus der Sperre, wird eine [**PHONE \_ STATE-Nachricht**](phone-state.md) an die Anwendung gesendet, um die Anwendung über die Zustandsänderung zu benachrichtigen. Parameter für diese Meldung geben einen Hinweis auf die Änderung an.

Die Lautstärke der Sprecherkomponente eines Hookswitch-Geräts kann mit [**phoneSetVolume festgelegt werden.**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) Die Lautstärkeeinstellung ist anders als stumm geschaltet, da die Lautstärkeeinstellung des Lautsprechers beibehalten wird, wenn ein Sprecher stummgeschaltet und später entmutiert wird. Die [**phoneGetVolume-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) kann verwendet werden, um die aktuelle Volumeeinstellung des Lautsprechers eines hookswitch-Geräts eines offenen Telefongeräts zurück zu geben.

Die Mikrofonkomponente eines Hookschaltergeräts kann ebenfalls gesteuert werden. Die Gain-Einstellung ist anders als stumm geschaltet, da das Stummschalten eines Mikrofons und das spätere Entmuting die Verstärkungseinstellung des Mikrofons beibehalten. Verwenden [**Sie phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) zum Festlegen des Mikrofons eines Hookswitchgeräts eines geöffneten Telefongeräts und [**phoneGetGain,**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) um die Verstärkungseinstellung des Mikrofons eines hookswitch-Geräts eines geöffneten Telefons zurückzuerhalten.

Wenn die Lautstärke oder der Gewinn des Hookswitchgeräts eines Telefons geändert wird, wird eine PHONE STATE-Nachricht an die Anwendungsfunktion gesendet, um die Anwendung über die \_ Zustandsänderung zu benachrichtigen. Parameter für diese Meldung geben einen Hinweis auf die Änderung an.

 

 



