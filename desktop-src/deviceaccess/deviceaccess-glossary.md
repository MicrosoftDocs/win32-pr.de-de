---
title: Glossar für den Gerätezugriff
description: Die folgenden Begriffe werden in der gesamten Dokumentation für die Geräte Zugriffs-API verwendet.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389820"
---
# <a name="device-access-glossary"></a>Glossar für den Gerätezugriff

Die folgenden Begriffe werden in der gesamten Dokumentation für die Geräte Zugriffs-API verwendet.

<dl> <dt>

**AppContainer**
</dt> <dd>

Eine stark eingeschränkte Ausführungsumgebung, in der ein Prozess mit einer verringerten Teilmenge der Berechtigungen des Benutzers ausgeführt wird. Ein Prozess, der in einem appcontainer ausgeführt wird, wird als appcontainer-Prozess bezeichnet. Ein appcontainer-Prozess ist von anderen appcontainer-Prozessen und vom Benutzerprofil isoliert. Der Zugriff auf eine sehr kleine Teilmenge von Systemressourcen wie Dateien, Geräte, Registrierungsschlüssel, IPC-Endpunkte (prozessübergreifende Communication, prozessübergreifende Communication) und Netzwerkressourcen ist beschränkt.

</dd> <dt>

**Binding**
</dt> <dd>

Zuordnen eines Geräte Zugriffs Objekts zu einer bestimmten Geräteschnittstelle Wenn die Bindung erfolgreich ist, können Windows Store-Apps das Geräte Zugriffs Objekt als Broker für die Kommunikation mit dem Gerätetreiber verwenden.

</dd> <dt>

**Broker**
</dt> <dd>

Eine Komponente, die Zugriff auf eine Ressource bereitstellt, die nicht standardmäßig erteilt wird.

</dd> <dt>

**Privilegierte App**
</dt> <dd>

Eine APP, die in den Metadaten eines bestimmten Geräts identifiziert wird, die dem Gerät zugeordnet ist, damit Sie mit der eingeschränkten Benutzeroberfläche des Gerätetreibers kommunizieren kann. Ein Beispiel für eine solche APP könnte eine proprietäre Musikwiedergabe-APP sein, die über exklusive Berechtigungen für die Synchronisierung mit einem tragbaren Musikplayer verfügt, wenn apps von Wettbewerbern dies nicht tun können. Weitere Informationen zum Festlegen der Metadaten eines Geräts oder zum Einschränken eines Treibers auf privilegierte apps finden Sie unter [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).

</dd> </dl>
