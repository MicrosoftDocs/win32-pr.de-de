---
title: Befehls Planung
description: Jedem Befehl ist eine Priorität zugeordnet.
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06512f0748aa88f6b32de3291e2ed1c262212ba2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341455"
---
# <a name="command-scheduling"></a>Befehls Planung

## <a name="command-scheduling"></a>Befehls Planung

Befehle können jederzeit aus mehreren Kontexten an die TSB übermittelt werden. Ein physisches TPM kann jedoch nur jeweils einen Befehl verarbeiten, und einige Befehle können für einen längeren Zeitraum ausgeführt werden. Wenn mehrere Befehle ausstehend sind, entscheidet der TSB, welcher Befehl an das TPM gesendet werden soll. Wenn ein Befehl übermittelt wird, ist jedem Befehl eine Priorität zugeordnet. Die TSB verwendet diese Prioritäten, um zu bestimmen, welcher ausstehende Befehl gesendet werden soll, wenn das TPM kostenlos ist. Die vier Prioritätsstufen sind niedrig, normal, hoch und System. Anwendungen sollten niedrige, normale oder hohe Priorität verwenden. Obwohl Befehle mit hoher Priorität üblicherweise vor Befehlen mit niedriger Priorität ausgeführt werden, hat der TSB-Befehls Planer eine Alterungs Richtlinie, die den Befehlen, die für einen längeren Zeitraum blockiert wurden, eine sehr hohe Priorität bietet.

## <a name="context-management"></a>Kontext Verwaltung

Wenn ein TPM \_ savecontext-oder TPM2 contextsave-Befehl mit einem virtuellen Handle an eine von TSB verwaltete Ressource übermittelt wird, führt der TSB den entsprechenden Befehl für die physische Ressource aus und gibt das Ergebnis an den Aufrufer zurück, wenn die Ressource physisch im TPM vorhanden ist. Wenn die Ressource nicht physisch im TPM vorhanden ist, bewirkt die Vorverarbeitung des TPM \_ savecontext-oder TPM2 \_ contextsave-Befehls, dass die Ressource erneut geladen wird. an diesem Punkt wird der Kontext gespeichert und an den Aufrufer zurückgegeben. Wenn die zu speichernde Ressource einen Typ hat, der nach dem Speichern normalerweise automatisch vom TPM geleert wird, wird die virtuelle Ressource von TSB bei Abschluss dieses Befehls ungültig. Wenn ein TPM- \_ loadcontext-oder TPM2 \_ contextload-Befehl an die TSB übermittelt wird, führt die TSB den Befehl sofort aus. Wenn der Befehl erfolgreich abgeschlossen wird, virtualisiert die TSB das Ressourcen Handle und übergibt den resultierenden TPM-Bytestream an den Aufrufer. Wenn ein TPM- \_ Befehl flushspecific oder TPM2 \_ flushcontext mit einem virtuellen Handle an eine von TSB verwaltete Ressource gesendet wird, führt die TSB einen TPM- \_ flushspecific-oder TPM2 \_ flushcontext-Befehl aus, um die Ressource aus dem TPM zu entfernen, wenn Sie physisch vorhanden ist. In diesem Fall macht die TSB die virtuelle Ressource ungültig und gibt das Ergebnis des Flush-Befehls an den Aufrufer zurück. Wenn die Ressource nicht physisch im TPM vorhanden ist, wird die Ressource, die dem virtuellen Handle entspricht, durch die Vorverarbeitung des TPM- \_ flushspecific-oder TPM2 \_ flushcontext-Befehls geladen. Sie wird dann geleert, wenn der Befehl tatsächlich verarbeitet wird. TSB bietet keine Unterstützung für das TPM \_ keycontrolowner-Bit oder die keephandle-Funktionalität des TPM \_ loadcontext-Vorgangs, sodass eine Ressource nicht das gleiche Handle erhält, das Sie vor dem Speichern des Kontexts besaß.

## <a name="other-commands"></a>Andere Befehle

Befehle, die in dieser Dokumentation nicht erwähnt werden, werden verarbeitet, indem die virtuellen Schlüssel Handles durch physische Schlüssel Handles (falls erforderlich) ersetzt und an das TPM übermittelt werden. Dies erfolgt nach dem Ausführen der entsprechenden Vorgänge, um sicherzustellen, dass die verwendeten Ressourcen physisch auf dem TPM vorhanden sind. Es wird keine zusätzliche besondere Verarbeitung durchgeführt. Die TSB versucht nicht, die Genauigkeit der Virtualisierung zu verbessern, indem die vom TPM zurückgegebenen Daten als Teil einer TPM \_ getcapability-oder TPM2 \_ getcapability-Abfrage geändert werden. Die TSB unterstützt auch die physischen TCG-Anwesenheits Befehle. Die TSB fungiert als Passthrough für Befehle für physische Präsenz. Es wird keine spezielle Verarbeitung durch die TSB selbst ausgeführt.

## <a name="cleanup"></a>Cleanup

Wenn ein Kontext beendet wird, werden alle zugeordneten physischen und virtuellen Ressourcen bereinigt, sodass keine Systemressourcen mehr beansprucht werden.

 

 




