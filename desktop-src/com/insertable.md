---
title: Insertable (CLSID-Schlüssel)
description: Gibt an, dass Objekte dieser Klasse im Listenfeld Objekt einfügen angezeigt werden sollen, wenn Sie von com-Container Anwendungen verwendet werden.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Insertable-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039994"
---
# <a name="insertable-clsid-key"></a>Insertable (CLSID-Schlüssel)

Gibt an, dass Objekte dieser Klasse im Listenfeld **Objekt einfügen** angezeigt werden sollen, wenn Sie von com-Container Anwendungen verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Bemerkungen

Dieser Schlüssel ist ein erforderlicher Eintrag für 32-Bit-COM-Anwendungen, deren Objekte in vorhandene 16-Bit-Anwendungen eingefügt werden können. Vorhandene 16-Bit-Anwendungen suchen in der Registrierung nach diesem Schlüssel, der der Anwendung mitteilt, dass der Server Einbettungen unterstützt. Wenn der **Insertable** -Schlüssel vorhanden ist, versuchen 16-Bit-Anwendungen möglicherweise auch, zu überprüfen, ob der Server auf dem Computer vorhanden ist. 16-Bit-Anwendungen rufen in der Regel den Wert des [**LocalServer**](localserver.md) -Schlüssels aus der-Klasse ab und überprüfen, ob es sich um eine gültige Datei im System handelt. Damit eine 32-Bit-Anwendung von einer 16-Bit-Anwendung einfügefähig ist, sollte die 32-Bit-Anwendung den **LocalServer** -Unterschlüssel zusätzlich zum Registrieren von [**LocalServer32**](localserver32.md)registrieren.

Dieser Eintrag wird mit-Steuerelementen verwendet und gibt an, dass ein Objekt nur als direktes eingebettetes Objekt ohne spezielle Steuerelement Funktionen fungieren kann. Objekte mit diesem Schlüssel werden im Dialogfeld **Objekt einfügen** für ihren Container angezeigt. Bei Verwendung mit-Steuerelementen gibt dieser Eintrag auch an, dass das Steuerelement mit nicht-Steuerelement Containern getestet wurde. Dieser Eintrag ist auch optional und kann ausgelassen werden, wenn ein Steuerelement nicht für die Arbeit mit älteren Containern konzipiert ist, die Steuerelemente nicht verstehen.

> [!Note]  
> Dieser Schlüssel ist nicht für interne Klassen wie die Monikerklassen vorhanden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




