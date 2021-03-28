---
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit GDI. Dieses Thema bietet Ihnen nicht alles, was Sie über Sicherheitsprobleme wissen müssen. Verwenden Sie Sie stattdessen als Ausgangspunkt und Verweis für diesen Technologiebereich.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Sicherheitsüberlegungen: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960195"
---
# <a name="security-considerations-gdi"></a>Sicherheitsüberlegungen: GDI

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit GDI. Dieses Thema bietet Ihnen nicht alles, was Sie über Sicherheitsprobleme wissen müssen. Verwenden Sie Sie stattdessen als Ausgangspunkt und Verweis für diesen Technologiebereich.

GDI weist in der Regel nur wenige Sicherheitsaspekte auf, da Sie anstelle von Eingaben angezeigt werden. Im folgenden finden Sie jedoch einige Punkte, die Sie berücksichtigen sollten.

Bitmaps, Metadateien und Schriftarten sind komplexe Strukturen, die beschädigt werden könnten. Es empfiehlt sich, zu versuchen, sicherzustellen, dass diese Elemente nicht beschädigt sind und aus einer vertrauenswürdigen Quelle stammen.

Eine Anwendung kann die Sicherheits Beschreibung für einige der Druck-und spoolingapis angeben. Beim Festlegen der Sicherheits Beschreibung sollten Sie sorgfältig vorgehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Security Central](https://www.microsoft.com/security/)
</dt> <dt>

[Security Developer Center](https://technet.microsoft.com/security/)
</dt> <dt>

[Sicherheits-TechCenter](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



