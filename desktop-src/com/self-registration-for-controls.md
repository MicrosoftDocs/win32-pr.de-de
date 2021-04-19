---
title: Selbstregistrierung für Steuerelemente
description: Selbstregistrierung für Steuerelemente
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339299"
---
# <a name="self-registration-for-controls"></a>Selbstregistrierung für Steuerelemente

ActiveX-Steuerelemente müssen die Selbstregistrierung unterstützen, indem die Funktionen [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) implementiert werden. ActiveX-Steuerelemente müssen alle Standard Registrierungseinträge für einbettbare Objekte und Automatisierungsserver registrieren.

ActiveX-Steuerelemente müssen die Komponenten Kategorien-API verwenden, um sich selbst als Steuerelement zu registrieren und die Komponenten Kategorien zu registrieren, die von einem Host unterstützt werden müssen, sowie alle Kategorien, die das Steuerelement implementiert, siehe [Komponenten Kategorien](component-categories.md).

ActiveX-Steuerelemente sollten auch den Registrierungsschlüssel [ToolBoxBitmap32](toolboxbitmap32.md) registrieren, obwohl dies nicht zwingend erforderlich ist.

Die Insertable-Komponenten Kategorie sollte nur registriert werden, wenn das Steuerelement als Verbund Dokument Objekt verwendet werden kann. Es ist wichtig zu beachten, dass ein Verbund Dokument Objekt bestimmte Schnittstellen unterstützen muss, die über die für ein ActiveX-Steuerelement erforderlichen minimalen [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) hinausgehen. Obwohl ein ActiveX-Steuerelement als Verbund Dokument Objekt qualifiziert sein kann, sollte die Dokumentation des Steuer Elements in den folgenden Situationen eindeutig angeben, welches Verhalten zu erwarten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

 