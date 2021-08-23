---
title: Einfügebar (CLSID-Schlüssel)
description: Gibt an, dass Objekte dieser Klasse im Dialogfeld Objekt einfügen angezeigt werden sollen, wenn sie von COM-Containeranwendungen verwendet werden.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Einfügebarer Registrierungsschlüssel (COM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c2d5d781545be05821b801b9e16048d2a097927890a63ead8f602c34d95613
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678590"
---
# <a name="insertable-clsid-key"></a>Einfügebar (CLSID-Schlüssel)

Gibt an, dass Objekte dieser Klasse im Dialogfeld Objekt **einfügen** angezeigt werden sollen, wenn sie von COM-Containeranwendungen verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Hinweise

Dieser Schlüssel ist ein erforderlicher Eintrag für 32-Bit-COM-Anwendungen, deren Objekte in vorhandene 16-Bit-Anwendungen eingefügt werden können. Vorhandene 16-Bit-Anwendungen suchen in der Registrierung nach diesem Schlüssel, wodurch die Anwendung darüber informiert wird, dass der Server Einbettungen unterstützt. Wenn der **einfügebare** Schlüssel vorhanden ist, versuchen 16-Bit-Anwendungen möglicherweise auch, zu überprüfen, ob der Server auf dem Computer vorhanden ist. 16-Bit-Anwendungen rufen in der Regel den Wert des [**LocalServer-Schlüssels**](localserver.md) aus der -Klasse ab und überprüfen, ob es sich um eine gültige Datei im System handelt. Damit eine 32-Bit-Anwendung von einer 16-Bit-Anwendung eingefügt werden kann, sollte die 32-Bit-Anwendung den **Unterschlüssel LocalServer** zusätzlich zur Registrierung von [**LocalServer32**](localserver32.md)registrieren.

Dieser Eintrag wird mit Steuerelementen verwendet und gibt an, dass ein Objekt nur als direkt eingebettetes Objekt ohne spezielle Steuerelementfunktionen fungieren kann. Objekte mit diesem Schlüssel werden im Dialogfeld **Objekt einfügen** für ihren Container angezeigt. Bei Verwendung mit Steuerelementen gibt dieser Eintrag auch an, dass das Steuerelement mit Containern ohne Steuerelement getestet wurde. Dieser Eintrag ist ebenfalls optional und kann weggelassen werden, wenn ein Steuerelement nicht für die Arbeit mit älteren Containern konzipiert ist, die steuerelemente nicht verstehen.

> [!Note]  
> Dieser Schlüssel ist für interne Klassen wie die Monikerklassen nicht vorhanden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




