---
description: Ein Telefongerät kann über mehrere Geräte vom Typ "Gerätewechsel" verfügen.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Gerätewechsel Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ad6f839ec9078831ffe0b04849be2a4393c9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527602"
---
# <a name="hookswitch-devices"></a>Gerätewechsel Geräte

Ein Telefongerät kann über mehrere Geräte vom Typ "Gerätewechsel" verfügen. Ein "huokswitch" ist der Schalter, der ein Gerät von der Telefonleitung verbindet oder trennt. Beispielsweise ist dies der Schalter, der automatisch aktiviert wird, wenn ein Benutzer den Empfänger von der Wiege auf einen neuen Wählton anhebt. TAPI definiert drei Typen von "huokswitch"-Geräten für ein Telefon: "Handy", "Speakerphone" und "Headset". Jedes Gerät für den Gerätewechsel verfügt über einen Sprecher und eine Mikrofon Komponente und arbeitet in einem von vier "huokswitch"-Modi:

-   **OnHook** Das Gerät "huokswitch" ist OnHook, und sowohl das Mikrofon als auch der Sprecher sind deaktiviert.
-   **Nur Mikrofon** Das Gerät "huokswitch" ist OFFHOOK, das Mikrofon ist aktiviert, und der Referent ist stumm.
-   **Nur Sprecher** Das Gerät für den Gerätewechsel ist OFFHOOK, das Mikrofon ist stumm und der Referent ist aktiviert.
-   **Mikrofon und Redner** Das Gerät "huokswitch" ist OFFHOOK, und sowohl das Mikrofon als auch der Sprecher sind aktiviert.

Die [**phonesethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) -Funktion wird verwendet, um den hookswitch-Modus eines oder mehrerer hookswitch-Geräte auf einem geöffneten Telefongerät festzulegen. Wenn Sie z. b. die Mikrofon-oder Lautsprecher Komponente eines Host Host Geräts stumm oder entstumm schalten möchten, verwenden Sie " **phonesethookswitch** " mit dem entsprechenden "Host"-Modus. Die [**phonegethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) -Funktion kann verwendet werden, um den hookswitch-Modus eines hookswitch-Geräts eines geöffneten Telefon Geräts abzufragen.

Wenn der Modus des Geräte-App-Geräts manuell geändert wird, z. b. durch das Übertragen des Telefons von seiner Wiege, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendung gesendet, um die Anwendung über die Statusänderung zu benachrichtigen. Die Parameter für diese Nachricht geben Aufschluss über die Änderung.

Das Volume der Redner Komponente eines "huokswitch"-Geräts kann mit " [**phonesetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)" festgelegt werden. Die volumeeinstellung unterscheidet sich von "stumm Schaltung" in, dass das stumm Schaltung eines Referenten und spätere entmutierung die Lautstärke Einstellung des Sprechers beibehält. Die Funktion " [**phonegetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) " kann verwendet werden, um die aktuelle volumeeinstellung des Sprechers eines hookswitch-Geräts eines geöffneten Telefon Geräts zurückzugeben.

Die Mikrofon Komponente eines "huokswitch"-Geräts kann auch durch einen Gewinn gesteuert werden. Der Wert für die Einstellung "gewinnen" unterscheidet sich von "stumm schalten", da der stumm Schaltung eines Mikrofons und spätere entmutierung die Einstellung für das Mikrofon beibehalten wird Verwenden Sie " [**phonesetget**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) ", um den Zuwachs des Mikrofons eines geöffnenden Telefon Geräts für ein geöffnetes Gerät festzulegen, und [**phonegetget**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) , um die erstellungseterlage eines geöffnenden Telefons für ein geöffnetes Telefon zurückzugeben.

Wenn das Volume oder der Gewinn des hookswitch-Geräts eines Telefons geändert wird, wird eine Telefon \_ Zustands Meldung an die Anwendungsfunktion gesendet, um die Anwendung über die Statusänderung zu benachrichtigen. Die Parameter für diese Nachricht geben Aufschluss über die Änderung.

 

 



