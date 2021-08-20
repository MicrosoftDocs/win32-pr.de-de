---
title: Befehlsplanung
description: Jedem Befehl ist eine Priorität zugeordnet.
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221702ee9dcebb8da454637f53cc29de1607d03088e24eb4a9a250d4e3ce2512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954438"
---
# <a name="command-scheduling"></a>Befehlsplanung

## <a name="command-scheduling"></a>Befehlsplanung

Befehle können jederzeit aus mehreren Kontexten an den TBS übermittelt werden. Ein physisches TPM kann jedoch nur einen Befehl nach dem anderen verarbeiten, und einige Befehle können für einen längeren Zeitraum ausgeführt werden. Wenn mehrere Befehle ausstehen, entscheidet tbs, welcher Befehl an das TPM gesendet werden soll. Wenn ein Befehl übermittelt wird, ist jedem Befehl eine Priorität zugeordnet. Der TBS verwendet diese Prioritäten, um zu bestimmen, welcher ausstehende Befehl übermittelt werden soll, wenn das TPM frei ist. Die vier Prioritätsebenen sind niedrig, normal, hoch und System. Anwendungen sollten eine niedrige, normale oder hohe Priorität verwenden. Obwohl Befehle mit hoher Priorität in der Regel vor Befehlen mit niedriger Priorität ausgeführt werden, verfügt der TBS-Befehlsplaner über eine veraltete Richtlinie, die schließlich Befehlen, die für längere Zeit blockiert wurden, eine sehr hohe Priorität einräumen.

## <a name="context-management"></a>Kontextverwaltung

Wenn ein TPM \_ SaveContext- oder TPM2 ContextSave-Befehl mit einem virtuellen Handle an eine Ressource übermittelt wird, die vom TBS verwalten wird, führt TBS den entsprechenden Befehl für die physische Ressource aus und gibt das Ergebnis an den Aufrufer zurück, wenn die Ressource physisch im TPM vorhanden ist. Wenn die Ressource nicht physisch im TPM vorhanden ist, bewirkt die Vorverarbeitung des BEFEHLs TPM SaveContext oder \_ TPM2 ContextSave, dass die Ressource erneut geladen wird. An diesem Punkt wird der Kontext gespeichert und an den \_ Aufrufer zurückgegeben. Wenn es sich bei der zu speichernden Ressource um einen Typ handelt, der normalerweise nach dem Speichern automatisch aus dem TPM geleert wird, macht TBS die virtuelle Ressource nach Abschluss dieses Befehls ungültig. Wenn ein TPM \_ LoadContext- oder TPM2 ContextLoad-Befehl an den TBS übermittelt wird, führt \_ TBS den Befehl sofort aus. Wenn der Befehl erfolgreich abgeschlossen wird, virtualisiert TBS das Ressourcenhand handle und übergibt den resultierenden TPM-Bytestream an den Aufrufer. Wenn ein TPM FlushSpecific- oder TPM2 FlushContext-Befehl mit einem virtuellen Handle an eine Ressource übermittelt wird, die der TBS verwalten soll, führt der TBS einen \_ \_ TPM \_ FlushSpecific- oder TPM2 FlushContext-Befehl aus, um die Ressource aus dem TPM zu löschen, wenn sie physisch vorhanden \_ ist. In diesem Fall macht TBS die virtuelle Ressource ungültig und gibt das Ergebnis des Flush-Befehls an den Aufrufer zurück. Wenn die Ressource nicht physisch im TPM vorhanden ist, wird die Ressource, die dem virtuellen Handle entspricht, bei der Vorverarbeitung des Tpm \_ FlushSpecific- oder TPM2 FlushContext-Befehls geladen. Sie wird jedoch geleert, wenn der Befehl tatsächlich verarbeitet \_ wird. Der TBS unterstützt das TPM KeyControlOwner-Bit oder die \_ keepHandle-Funktionalität des TPM LoadContext-Vorgangs nicht, sodass eine Ressource nicht das gleiche Handle wie vor dem Speichern des Kontexts erhalten \_ hat.

## <a name="other-commands"></a>Andere Befehle

Befehle, die in dieser Dokumentation nicht erwähnt werden, werden verarbeitet, indem virtuelle Schlüsselhandles durch physische Schlüsselhandles (falls erforderlich) ersetzt und an das TPM übermitteln werden. Dies erfolgt nach dem Ausführen der entsprechenden Vorgänge, um sicherzustellen, dass die verwendeten Ressourcen physisch auf dem TPM vorhanden sind. Es wird keine zusätzliche spezielle Verarbeitung ausgeführt. TbS versucht nicht, die Genauigkeit der Virtualisierung zu verbessern, indem die vom TPM im Rahmen einer TPM \_ GetCapabilities- oder TPM2 GetCapability-Abfrage zurückgegebenen Daten \_ geändert werden. TbS unterstützt auch TCG Physical Presence-Befehle. TbS fungiert als Pass-Through für Physische Anwesenheitsbefehle. Vom TBS selbst wird keine spezielle Verarbeitung ausgeführt.

## <a name="cleanup"></a>Bereinigen

Wenn ein Kontext beendet wird, werden alle ihm zugeordneten physischen und virtuellen Ressourcen bereinigt, damit sie keine Systemressourcen mehr verbrauchen.

 

 




