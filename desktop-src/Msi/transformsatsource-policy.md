---
description: Wenn diese benutzerspezifische Systemrichtlinie auf &\# 0034;1&0034; festgelegt ist, sucht das Installationsprogramm im Stammverzeichnis aller Netzwerkquellen in der Quellliste nach Transformationsdateien für das \# Produkt. Standardmäßig werden Transformationen im Ordner Anwendungsdaten des Profils eines Benutzers gespeichert.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: TransformsAtSource-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab909fd728ce1cebba894dd8598879fa055ce762ed027cd8842cc7236a0f24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623479"
---
# <a name="transformsatsource-policy"></a>TransformsAtSource-Richtlinie

Wenn diese benutzerspezifische [Systemrichtlinie](system-policy.md) auf "1" festgelegt ist; Das Installationsprogramm sucht im Stammverzeichnis aller Netzwerkquellen in der Quellliste für das Produkt nach Transformationsdateien. Standardmäßig werden Transformationen im Ordner Anwendungsdaten des Profils eines Benutzers gespeichert.

Windows Das Installationsprogramm interpretiert die TransformsAtSource-Richtlinie so, dass sie mit der [TransformsSecure-Richtlinie identisch ist.](transformssecure-policy.md)

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ SZ**

 

 



