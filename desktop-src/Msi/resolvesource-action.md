---
description: Die ResolveSource-Aktion bestimmt den Speicherort der Quelle und legt die SourceDir-Eigenschaft fest, wenn die Quelle noch nicht aufgelöst wurde.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: ResolveSource-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350056"
---
# <a name="resolvesource-action"></a>ResolveSource-Aktion

Die ResolveSource-Aktion bestimmt den Speicherort der Quelle und legt die [**SourceDir**](sourcedir.md) -Eigenschaft fest, wenn die Quelle noch nicht aufgelöst wurde.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die ResolveSource-Aktion muss nach der [costinitialize-Aktion](costinitialize-action.md)erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die ResolveSource-Aktion muss vor der Verwendung der [**SourceDir**](sourcedir.md) -Eigenschaft in einem beliebigen Ausdruck aufgerufen werden. Es muss auch aufgerufen werden, bevor versucht wird, den Wert der **SourceDir** -Eigenschaft mithilfe von " [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)" abzurufen. Die ResolveSource-Aktion sollte nicht ausgeführt werden, wenn die Quelle nicht verfügbar ist, da Sie möglicherweise beim Deinstallieren der Anwendung vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 



