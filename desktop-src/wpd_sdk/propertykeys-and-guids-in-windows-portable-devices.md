---
description: PROPERTYKEYs und GUIDs in Windows Portable Devices
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs und GUIDs in Windows Portable Devices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80100b043383074f58bc27fe8e9782c4fd6d2e4f3841a28f37035f39d23cc7c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054870"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs und GUIDs in Windows Portable Devices

Eine Eigenschaft oder ein Befehl wird durch eine PROPERTYKEY-Struktur identifiziert. Eine PROPERTYKEY-Struktur besteht aus zwei Teilen: einer GUID (dem fmtid-Member) und einem DWORD (pid-Member). Der GUID-Teil wird verwendet, um die Kategorie anzugeben, zu der die Eigenschaft oder der Befehl gehört (d. h., verwandte Eigenschaften gehören zur gleichen Kategorie, und verwandte Befehle gehören derselben Kategorie an. Daher weisen sie denselben fmtid auf). Der DWORD-Teil gibt die Eigenschaft oder Befehls-ID an und wird verwendet, um die einzelnen Eigenschaften oder Befehle innerhalb einer Eigenschaft oder Befehlskategorie zu unterscheiden (d. h., die Pid-Werte für Eigenschaften oder Befehle in derselben Kategorie unterscheiden sich).

Im Referenzabschnitt dieses Dokuments werden alle PROPERTYKEY-Werte beschrieben, die von WPD definiert werden. diese Werte entsprechen Befehlen, Eigenschaften und Ressourcen. Wenn Sie einen benutzerdefinierten PROPERTYKEY-Wert erstellen, sollten Sie eine neue **GUID-Kategorie** definieren. Verwenden Sie die **WPD-GUID-Werte** nicht wieder, oder Sie riskieren einen Konflikt mit vorhandenen und zukünftigen WPD-angegebenen PROPERTYKEYs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungsübersicht**](application-overview.md)
</dt> <dt>

[**Befehle**](commands.md)
</dt> <dt>

[**Objektformat-GUIDs**](object-format-guids.md)
</dt> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



